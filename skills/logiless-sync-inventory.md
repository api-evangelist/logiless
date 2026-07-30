---
name: Sync products and read inventory
description: Register products (articles) in LOGILESS and read logical and actual (storage) inventory levels.
api: openapi/logiless-openapi.yml
operations: [listArticles, createArticle, listLogicalInventorySummaries, listActualInventorySummaries]
---

# Sync products and read inventory (商品・在庫)

Keep a product catalog in sync with LOGILESS and read current stock. All paths are scoped to `/api/v1/merchant/{merchant_id}/...`.

## Prerequisites
- OAuth 2.0 Bearer token (`authentication/logiless-authentication.yml`) and the `merchant_id`.

## Steps
1. **List existing products** — `listArticles` `GET /merchant/{merchant_id}/articles`; page through `data[]` with `limit`/`page`.
2. **Create or update** — `createArticle` `POST /merchant/{merchant_id}/articles/new` (or `createArticlesMultiple` for bulk); `updateArticle` `PUT /merchant/{merchant_id}/articles/{id}`; remove with `deleteArticle` `DELETE /merchant/{merchant_id}/articles/{id}/delete`.
3. **Read logical inventory** — `listLogicalInventorySummaries` `GET /merchant/{merchant_id}/logical_inventory_summaries` for available/reserved quantities; bulk lookup via `searchLogicalInventorySummaries` (`.../search`) by ids/codes.
4. **Read storage inventory** — `listActualInventorySummaries` `GET /merchant/{merchant_id}/actual_inventory_summaries` for physical stock per warehouse; bulk via `searchActualInventorySummaries`.

## Rules
- `limit` max is 500 (raised from 100 on 2026-06-11); default 20. Use `page` to walk pages.
- Some fields (e.g. `inventory_segment_name`, `transferring`, `logical_reserved`) appear only when the merchant uses the corresponding LOGILESS feature.
- Rate limit ~1 req/sec; honor `X-RateLimit-*` headers and 429 backoff.
