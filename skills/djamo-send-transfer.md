---
name: Send money with Djamo
description: Verify a recipient, send a single or batch transfer, and reconcile status via webhook or polling.
api: Djamo Business API
source: https://docs.djamo.com/api/transfer.html
operations:
  - GET /v1/transactions/customers/check
  - POST /v1/transactions
  - POST /v1/transactions/batch
  - GET /v1/transactions/:id
  - GET /v1/balance
---

# Send money with Djamo

Use this skill to disburse money to one or many recipients via the Djamo Business API.

## Auth
- `Authorization: Bearer <ACCESS_TOKEN>` on every request, HTTPS only. Some endpoints also require `X-company-Id`.

## Steps
1. **Check balance** — `GET /v1/balance` returns `balance` and `currency` (XOF). Ensure funds cover amount + fee.
2. **Verify the recipient** — `GET /v1/transactions/customers/check?msisdn={E.164}` confirms the number is a Djamo customer.
3. **Send a single transfer** — `POST /v1/transactions` with `msisdn` (E.164), `amount` (5,000–500,000 XOF), `type: "transfer"`, and a unique `reference` (idempotency key; duplicate reference → 409). Response returns `id`, `fee`, `totalAmount`, `status` (`pending`), and `djamoTransactionReference`.
4. **Or send in bulk** — `POST /v1/transactions/batch` with a `transactions` array; response has a `batchId` and per-transaction records.
5. **Reconcile** — handle `transactions/started|completed|failed` webhooks (verify `x-djamo-hmac-sha256`) or poll `GET /v1/transactions/:id` (or `?reference={value}`). On failure read `failureReason`.

## Rules
- Idempotency: always send a unique `reference`; treat 409 as "already submitted" and look it up by reference rather than resending.
- Respect the 5,000–500,000 XOF per-transfer bounds. Back off on 429; log `correlationId` on errors.
