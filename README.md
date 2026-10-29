# Bokio

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

Bokio is a Swedish cloud accounting and bookkeeping platform (a Visma company) for small businesses, sole traders and their accountants, combining automated bookkeeping, invoicing, a business bank account and financial reporting. Its public REST API is split into a Company API (journal entries, invoices, credit notes, customers, items, suppliers and supplier invoices, uploads, bank payments, chart of accounts, fiscal years and SIE export) and a General API that handles OAuth 2.0 token issuance and connection management for public multi-tenant integrations. Authentication is OAuth 2.0 (authorization code and client credentials) with 24 fine-grained resource:action scopes; the API uses URI-path versioning (v1), page-number pagination, per-token rate limits and a documented deprecation, brownout and sunset lifecycle.

**Areas:** Company · Fintech · Accounting · Bookkeeping · Invoicing · Payments · Sweden · Small Business · Authentication

## Bokio on APIs.io

Everything profiled for Bokio is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bokio/](https://apis.io/providers/bokio/)** — or go straight to one of the APIs or properties below.

### APIs (16)

- [Bokio Authorization API](https://apis.io/apis/bokio/bokio-authorization-api/) — Authorization operations for OAuth 2.0 Grants
- [Bokio Bank Payments API](https://apis.io/apis/bokio/bokio-bank-payments-api/) — Operations for creating and reading bank payments
- [Bokio Chart Of Accounts API](https://apis.io/apis/bokio/bokio-chart-of-accounts-api/) — Operations for managing chart of accounts
- [Bokio Company Information API](https://apis.io/apis/bokio/bokio-company-information-api/) — Operations for managing company information
- [Bokio Connections API](https://apis.io/apis/bokio/bokio-connections-api/) — Connections operations
- [Bokio Credit Notes API](https://apis.io/apis/bokio/bokio-credit-notes-api/) — Operations for managing credit notes
- [Bokio Customers API](https://apis.io/apis/bokio/bokio-customers-api/) — Operations for managing customer data
- [Bokio Fiscal Years API](https://apis.io/apis/bokio/bokio-fiscal-years-api/) — Operations for managing fiscal years
- [Bokio Invoices API](https://apis.io/apis/bokio/bokio-invoices-api/) — Operations for managing invoices
- [Bokio Items API](https://apis.io/apis/bokio/bokio-items-api/) — Operations for managing inventory items
- [Bokio Journal Entries API](https://apis.io/apis/bokio/bokio-journal-entries-api/) — Operations for managing accounting journal entries
- [Bokio Sie Files API](https://apis.io/apis/bokio/bokio-sie-files-api/) — Operations for managing SIE files
- [Bokio Supplier Invoices API](https://apis.io/apis/bokio/bokio-supplier-invoices-api/) — Operations for managing supplier invoices
- [Bokio Suppliers API](https://apis.io/apis/bokio/bokio-suppliers-api/) — Operations for managing suppliers
- [Bokio Tag Groups API](https://apis.io/apis/bokio/bokio-tag-groups-api/) — Operations for managing tag groups and tags
- [Bokio Uploads API](https://apis.io/apis/bokio/bokio-uploads-api/) — Operations for managing file uploads

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [bokio](https://apis.io/servers/bokio/bokio/)

#### Collections (32)

Postman and Open Collection request collections.

- [Company authorization API](https://apis.io/collections/bokio/open-bokio-authorization-api/)
- [Company authorization bank-payments API](https://apis.io/collections/bokio/open-bokio-bank-payments-api/)
- [Company authorization chart-of-accounts API](https://apis.io/collections/bokio/open-bokio-chart-of-accounts-api/)
- [Company authorization company-information API](https://apis.io/collections/bokio/open-bokio-company-information-api/)
- [Company authorization connections API](https://apis.io/collections/bokio/open-bokio-connections-api/)
- [Company authorization credit-notes API](https://apis.io/collections/bokio/open-bokio-credit-notes-api/)
- [Company authorization customers API](https://apis.io/collections/bokio/open-bokio-customers-api/)
- [Company authorization fiscal-years API](https://apis.io/collections/bokio/open-bokio-fiscal-years-api/)
- [Company authorization invoices API](https://apis.io/collections/bokio/open-bokio-invoices-api/)
- [Company authorization items API](https://apis.io/collections/bokio/open-bokio-items-api/)
- [Company authorization journal-entries API](https://apis.io/collections/bokio/open-bokio-journal-entries-api/)
- [Company authorization sie-files API](https://apis.io/collections/bokio/open-bokio-sie-files-api/)
- [Company authorization supplier-invoices API](https://apis.io/collections/bokio/open-bokio-supplier-invoices-api/)
- [Company authorization suppliers API](https://apis.io/collections/bokio/open-bokio-suppliers-api/)
- [Company authorization tag-groups API](https://apis.io/collections/bokio/open-bokio-tag-groups-api/)
- [Company authorization uploads API](https://apis.io/collections/bokio/open-bokio-uploads-api/)
- [Company authorization API](https://apis.io/collections/bokio/postman-bokio-authorization-api/)
- [Company authorization bank-payments API](https://apis.io/collections/bokio/postman-bokio-bank-payments-api/)
- [Company authorization chart-of-accounts API](https://apis.io/collections/bokio/postman-bokio-chart-of-accounts-api/)
- [Company authorization company-information API](https://apis.io/collections/bokio/postman-bokio-company-information-api/)
- [Company authorization connections API](https://apis.io/collections/bokio/postman-bokio-connections-api/)
- [Company authorization credit-notes API](https://apis.io/collections/bokio/postman-bokio-credit-notes-api/)
- [Company authorization customers API](https://apis.io/collections/bokio/postman-bokio-customers-api/)
- [Company authorization fiscal-years API](https://apis.io/collections/bokio/postman-bokio-fiscal-years-api/)
- [Company authorization invoices API](https://apis.io/collections/bokio/postman-bokio-invoices-api/)
- …and 7 more published on APIs.io

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Bokio Company Api Overlay](https://apis.io/overlays/bokio/bokio-company-api-overlay/)
- [Bokio General Api Overlay](https://apis.io/overlays/bokio/bokio-general-api-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Bokio Authentication](https://apis.io/security/bokio/bokio-authentication/)
- [Bokio Domain Security](https://apis.io/security/bokio/bokio-domain-security/)
- [Bokio Trust Center](https://apis.io/security/bokio/bokio-trust-center/)
- [Bokio Vulnerability Disclosure](https://apis.io/security/bokio/bokio-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Bokio Scopes](https://apis.io/scopes/bokio/bokio-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://bokio.se/)
- [Documentation](https://docs.bokio.se/)
- [Getting started](https://docs.bokio.se/docs/welcome)
- [API reference](https://docs.bokio.se/reference/overview)
- [Pricing](https://www.bokio.se/priser/)
- [Sign up](https://app.bokio.se/sign-up)
- [Blog](https://www.bokio.se/blogg/)
- [Security](https://www.visma.com/trust-centre/security/products-and-services/bug-bounty-and-responsible-disclosure/)
- [Terms of service](https://docs.bokio.se/page/terms/)
- [Privacy policy](https://www.bokio.se/villkor-och-gdpr/integritetspolicy/)
- [GitHub](https://github.com/bokio)

## API Evangelist rating

**Kin Score 45.7** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 52.4 |
| Contract governance | 4.5 |
| Operational transparency | 32.9 |
| Developer ergonomics | 43.5 |
| Access clarity | 47.4 |

**Agent readiness 33.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 39.3** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bokio/](https://apis.io/providers/bokio/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Bokio: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bokio/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
