---
name: Register and track inbound stock
description: Create inbound delivery (purchase receipt) records in LOGILESS, track them, and manage suppliers.
api: openapi/logiless-openapi.yml
operations: [createInboundDelivery, listInboundDeliveries, reverseInboundDelivery, listSuppliers]
---

# Register and track inbound stock (入荷予定)

Record expected inbound shipments so warehouse receiving and inventory stay accurate. All paths are scoped to `/api/v1/merchant/{merchant_id}/...`.

## Prerequisites
- OAuth 2.0 Bearer token (`authentication/logiless-authentication.yml`) and the `merchant_id`.

## Steps
1. **Resolve the supplier** — `listSuppliers` `GET /merchant/{merchant_id}/suppliers`; create one with `createSupplier` (`.../suppliers/new`) if missing.
2. **Create the inbound delivery** — `createInboundDelivery` `POST /merchant/{merchant_id}/inbound_deliveries/new` with the expected articles, quantities and target warehouse. Line fields such as `scheduled_delivery_date` and `inventory_segment_name` are available where the feature is enabled.
3. **Track** — `listInboundDeliveries` `GET /merchant/{merchant_id}/inbound_deliveries`, filtering by `updated_at_from`/`updated_at_to`.
4. **Reverse a mistake** — `reverseInboundDelivery` `POST /merchant/{merchant_id}/inbound_deliveries/{id}/reversal`.

## Rules
- Pagination via `limit` (max 500) + `page`; results in `data[]`.
- No idempotency key; avoid re-posting the same inbound delivery.
- Rate limit ~1 req/sec; back off on 429 using `X-RateLimit-Reset`.
- Errors follow the shared envelope (`errors/logiless-problem-types.yml`).
