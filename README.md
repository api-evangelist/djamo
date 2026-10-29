# Djamo

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Djamo is a mobile-first fintech serving Côte d'Ivoire and Sénégal, giving 1.5M+ users current and savings accounts with an IBAN, virtual and physical Visa cards, money transfers to Mobile Money and bank accounts, bill payments, short-term credit, and BRVM investment products. For businesses, Djamo exposes a REST Business API that lets companies collect payments ("Pay with Djamo"), send single and mass transfers to recipients by phone number, check their real-time balance, and manage marketplace sub-companies, secured with bearer tokens and HMAC-signed webhooks. Djamo is a Y Combinator alumnus backed by investors including Partech.

**Areas:** Company · Financial Services · Fintech · Payments · Banking · Money Transfer · Africa · Côte d'Ivoire · Sénégal

## Djamo on APIs.io

Everything profiled for Djamo is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/djamo/](https://apis.io/providers/djamo/)** — or go straight to one of the APIs or properties below.

### APIs (1)

- [Djamo Business API](https://apis.io/apis/djamo/djamo-business-api/) — REST API for businesses to collect payments, send single and mass transfers, check balance, manage sub-companies, and receive HMAC-signed webhooks.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Djamo Business API Webhooks](https://apis.io/asyncapis/djamo/djamo-webhooks-asyncapi/)

#### Event channels (4)

Individual events and webhooks the provider emits.

- [charge/events](https://apis.io/channels/djamo/charge-events/)
- [transactions/completed](https://apis.io/channels/djamo/transactions-completed/)
- [transactions/failed](https://apis.io/channels/djamo/transactions-failed/)
- [transactions/started](https://apis.io/channels/djamo/transactions-started/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [djamo](https://apis.io/servers/djamo/djamo/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Djamo Authentication](https://apis.io/security/djamo/djamo-authentication/)
- [Djamo Domain Security](https://apis.io/security/djamo/djamo-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.djamo.com/)
- [Pricing](https://www.djamo.com/fr-ci/tarifs-business)
- [Sign up](https://go.djamo.com/app)
- [Support](https://docs.djamo.com/contact.html)
- [Blog](https://www.djamo.com/fr-ci/apprendre)
- [Terms of service](https://www.djamo.com/fr-ci/conditions-generales-et-tarifaires)
- [Privacy policy](https://www.djamo.com/fr-ci/politique-de-confidentialite)

## API Evangelist rating

**Kin Score 41.6** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 42.7 |
| Contract governance | 4.5 |
| Operational transparency | 7.9 |
| Developer ergonomics | 66.1 |
| Access clarity | 44.7 |

**Agent readiness 23.6** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 19.7** — Banking & Open Finance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/djamo/](https://apis.io/providers/djamo/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Djamo: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/djamo/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
