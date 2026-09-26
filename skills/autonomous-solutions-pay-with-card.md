---
name: autonomous-solutions-pay-with-card
description: Process a card payment for a user by creating a setup intent, attaching the payment method, executing the payment, and confirming
  it.
api: openapi/autonomous-solutions-openapi.json
operations:
- get_setup_intent_users_payments_setup_intent_post
- attach_payment_method_users_payments_save_payment_method_post
- pay_with_card_users_payments_pay_post
- confirm_payment_users_payments_confirm_payment_post
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/autonomous-solutions-openapi.json ; every operationId checked against the contract
---

# autonomous-solutions-pay-with-card

Process a card payment for a user by creating a setup intent, attaching the payment method, executing the payment, and confirming it.

## Steps

1. 1. Call `get_setup_intent_users_payments_setup_intent_post` with the required request body fields for creating a setup intent.
2. 2. Call `attach_payment_method_users_payments_save_payment_method_post` with the setup intent ID and payment method details.
3. 3. Call `pay_with_card_users_payments_pay_post` providing the payment method ID and amount to charge.
4. 4. Call `confirm_payment_users_payments_confirm_payment_post` with the payment ID to finalize the transaction.

## Rules

- Rate limit: 360 requests per minute; exceeding returns HTTP 429.
- Pagination for list endpoints uses a cursor-based approach.
