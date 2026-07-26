---
name: Collect a payment with Djamo
description: Create a Pay-with-Djamo charge, redirect the customer to pay, and confirm settlement via webhook or polling.
api: Djamo Business API
source: https://docs.djamo.com/api/collection.html
operations:
  - POST /v1/charges
  - GET /v1/charges/:id
  - POST /v1/charges/:id/refund
---

# Collect a payment with Djamo

Use this skill to collect a payment from a customer via the Djamo Business API.

## Auth
- Send `Authorization: Bearer <ACCESS_TOKEN>` (token prefix `at_`) on every request; HTTPS only.
- The token + base URL decide staging vs production. Staging base: `https://apibusiness-staging-civ.djamo.io` (CIV) / `https://apibusiness-staging-sen.djamo.io` (SEN). Production: `https://api-civ.djamo.com` / `https://api-sen.djamo.com`.

## Steps
1. **Create the charge** — `POST /v1/charges` with `amount` (positive integer, XOF, no decimals), a unique `externalId` (your reference — reusing it for a different charge returns HTTP 409), `description`, `onCompletedRedirectionUrl`, and `onCanceledRedirectionUrl`. Optional `metadata`.
2. **Redirect the customer** — send them to the returned `paymentUrl`. Mobile users open the Djamo app; web users scan a QR. The charge is `due` for ~1 hour.
3. **Confirm settlement** — either handle the `charge/events` webhook (verify the `x-djamo-hmac-sha256` HMAC-SHA256 signature against the raw body with your `SECRET_KEY`) or poll `GET /v1/charges/:id`. Terminal states: `paid`, `refunded`, `refunded_partially`, `dropped`.
4. **Refund if needed** — `POST /v1/charges/:id/refund` for a full or partial refund.
5. **(Staging only)** simulate payment with `POST /v1/charges/:id/pay` to drive a charge to `paid` without the app.

## Rules
- Idempotency: always send a unique `externalId`; treat 409 as "already created".
- On 429 back off exponentially. On 401/403 re-check the token. Errors carry a `correlationId` — log it for support.
