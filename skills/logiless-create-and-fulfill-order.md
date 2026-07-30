---
name: Create and fulfill a sales order
description: Create a sales order in LOGILESS, move it through confirmation, and track its outbound shipment.
api: openapi/logiless-openapi.yml
operations: [createSalesOrder, confirmSalesOrder, listOutboundDeliveries, reverseSalesOrder]
---

# Create and fulfill a sales order (受注 → 出荷)

Use this to push an e-commerce order into LOGILESS and follow it to shipment. All paths are scoped to a merchant: `/api/v1/merchant/{merchant_id}/...`.

## Prerequisites
- An OAuth 2.0 Bearer access token (see `authentication/logiless-authentication.yml`). Send `Authorization: Bearer {access_token}`.
- The `merchant_id` the token is scoped to.
- Requests/responses are JSON; UTF-8 with `\uNNNN`-escaped Japanese.

## Steps
1. **Create the order** — `createSalesOrder` `POST /merchant/{merchant_id}/sales_orders/new`.
   Required fields: `code` (受注コード), `buyer_name1`, `recipient_name1`, `recipient_address1`. `document_status`, `allocation_status`, `delivery_status` are read-only and set by LOGILESS. Add line items in `lines[]`.
   - To load many orders at once use `createSalesOrdersMultiple` (`.../new/multiple`).
2. **Confirm** — if the order was created in a pending-confirmation state, call `createSalesOrderConfirmation` then `confirmSalesOrder` to release it for allocation/fulfillment.
3. **Track shipment** — poll `listOutboundDeliveries` `GET /merchant/{merchant_id}/outbound_deliveries` filtered by `updated_at_from`/`updated_at_to`; match to your order.
4. **Cancel if needed** — `reverseSalesOrder` `POST /merchant/{merchant_id}/sales_orders/{id}/reversal`. If the order's `document_status` no longer allows changes you will get HTTP 423.

## Rules
- No idempotency-key: guard against duplicates using a unique `code`. A create with an existing `code` is rejected unless you set the allow-duplicate flag.
- Pagination: `limit` (default 20, max 500) + `page` (default 1); read results from `data[]`.
- Rate limit: keep to ~1 req/sec; on HTTP 429 back off using `X-RateLimit-Reset`.
- Errors: 400 returns `{code,message,errors{}}`; other statuses return `{error,error_description}` (see `errors/logiless-problem-types.yml`).
