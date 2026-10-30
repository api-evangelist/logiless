# Logiless

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

LOGILESS (ロジレス) is a Japanese cloud EC logistics platform that unifies order management (OMS) and warehouse management (WMS) for e-commerce merchants — automating order intake from marketplaces and shopping carts (Rakuten, Shopify, ColorMe, futureshop, ec-force and more), inventory synchronization, allocation, shipping-label issuance and warehouse operations. LOGILESS exposes a RESTful, OAuth2-protected API (scoped per merchant) for reading and writing sales orders, outbound and inbound deliveries, sales returns, inter-warehouse transfers, articles (product master), multi-layer inventory summaries, warehouses, stores and suppliers. The company is a 500 Global portfolio company. This profile was enriched by the API Evangelist pipeline from LOGILESS's public developer documentation; the OpenAPI here is derived and not an official LOGILESS artifact.

**Areas:** Logistics · E-Commerce · Order Management · Warehouse Management · Inventory · Fulfillment · Shipping · OMS · WMS · Japan

## Logiless on APIs.io

Everything profiled for Logiless is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/logiless/](https://apis.io/providers/logiless/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [Logiless Articles API](https://apis.io/apis/logiless/logiless-articles-api/) — 商品マスタ / 商品対応表 — product master and mapping
- [Logiless Inbound Deliveries API](https://apis.io/apis/logiless/logiless-inbound-deliveries-api/) — 入荷予定伝票 — expected inbound shipments
- [Logiless Inter-Warehouse Transfers API](https://apis.io/apis/logiless/logiless-inter-warehouse-transfers-api/) — 倉庫間移動伝票 — stock transfers between warehouses
- [Logiless Inventory API](https://apis.io/apis/logiless/logiless-inventory-api/) — 在庫 / 保管状況 / 日次在庫表 / 在庫操作ログ / 倉庫別発注点 — inventory & storage summaries
- [Logiless Locations API](https://apis.io/apis/logiless/logiless-locations-api/) — 店舗 / 倉庫 / ロケーション — stores, warehouses and locations
- [Logiless Outbound Deliveries API](https://apis.io/apis/logiless/logiless-outbound-deliveries-api/) — 出荷伝票 — shipment records
- [Logiless Sales Orders API](https://apis.io/apis/logiless/logiless-sales-orders-api/) — 受注伝票 — order intake, editing, confirmation and reversal
- [Logiless Sales Returns API](https://apis.io/apis/logiless/logiless-sales-returns-api/) — 売上返品 — returns
- [Logiless Suppliers API](https://apis.io/apis/logiless/logiless-suppliers-api/) — 仕入先マスタ — supplier master

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [logiless](https://apis.io/servers/logiless/logiless/)

#### Collections (9)

Postman and Open Collection request collections.

- [LOGILESS Articles API](https://apis.io/collections/logiless/open-logiless-articles-api/)
- [LOGILESS Articles Inbound Deliveries API](https://apis.io/collections/logiless/open-logiless-inbound-deliveries-api/)
- [LOGILESS Articles Inter-Warehouse Transfers API](https://apis.io/collections/logiless/open-logiless-inter-warehouse-transfers-api/)
- [LOGILESS Articles Inventory API](https://apis.io/collections/logiless/open-logiless-inventory-api/)
- [LOGILESS Articles Locations API](https://apis.io/collections/logiless/open-logiless-locations-api/)
- [LOGILESS Articles Outbound Deliveries API](https://apis.io/collections/logiless/open-logiless-outbound-deliveries-api/)
- [LOGILESS Articles Sales Orders API](https://apis.io/collections/logiless/open-logiless-sales-orders-api/)
- [LOGILESS Articles Sales Returns API](https://apis.io/collections/logiless/open-logiless-sales-returns-api/)
- [LOGILESS Articles Suppliers API](https://apis.io/collections/logiless/open-logiless-suppliers-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Logiless Overlay](https://apis.io/overlays/logiless/logiless-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Logiless Authentication](https://apis.io/security/logiless/logiless-authentication/)
- [Logiless Domain Security](https://apis.io/security/logiless/logiless-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Logiless Scopes](https://apis.io/scopes/logiless/logiless-scopes/)

#### Rate limits (1)

Published request limits.

- [Logiless Rate Limits](https://apis.io/rate-limits/logiless/logiless-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.logiless.com)
- [Documentation](https://support.logiless.com/)
- [Getting started](https://app2.logiless.com/developer/documents/authentication)
- [API reference](https://app2.logiless.com/developer/documents/specifications)
- [Pricing](https://www.logiless.com/price/)
- [Sign up](https://app2.logiless.com/merchant/sign_up)
- [Support](https://support.logiless.com/)
- [Blog](https://www.logiless.com/blog/)
- [Terms of service](https://www.logiless.com/legal/terms/)
- [Privacy policy](https://www.logiless.com/legal/privacy-policy/)

## API Evangelist rating

**Kin Score 38.4** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 11.6 |
| Contract governance | 4.5 |
| Operational transparency | 36.8 |
| Developer ergonomics | 58.9 |
| Access clarity | 44.7 |

**Agent readiness 31.0** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | verified |
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

**Regulatory alignment 34.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/logiless/](https://apis.io/providers/logiless/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Logiless: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/logiless/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
