---
name: autonomous-solutions-create-and-check-order
description: Create a new order for a user and verify if it is ready for checkout.
api: openapi/autonomous-solutions-openapi.json
operations:
- create_user_order_users__user_id__orders_post
- check_user_order_available_to_checkout_users__user_id__orders__order_id__checkout_available_get
- get_user_order_by_id_users__user_id__orders__order_id__get
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/autonomous-solutions-openapi.json ; every operationId checked against the contract
---

# autonomous-solutions-create-and-check-order

Create a new order for a user and verify if it is ready for checkout.

## Steps

1. 1. Use `create_user_order_users__user_id__orders_post` with required body fields for the new order.
2. 2. Use `check_user_order_available_to_checkout_users__user_id__orders__order_id__checkout_available_get` with path parameters `user_id` and `order_id` returned from step 1.
3. 3. (Optional) Use `get_user_order_by_id_users__user_id__orders__order_id__get` to retrieve the order details after checkout availability is confirmed.

## Rules

- Include the authentication header as required by the API (e.g., `Authorization: Bearer <token>`).
- Respect the rate limit of 360 requests per minute; exceeding it returns HTTP 429.
- Pagination uses a cursor‑based approach for list endpoints.
