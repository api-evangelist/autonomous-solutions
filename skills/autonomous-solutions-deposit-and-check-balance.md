---
name: autonomous-solutions-deposit-and-check-balance
description: Deposit funds into a user's wallet and verify the updated balance.
api: openapi/autonomous-solutions-openapi.json
operations:
- create_wallet_deposit_users_wallet_deposit_post
- get_wallet_balance_users_wallet_balance_get
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/autonomous-solutions-openapi.json ; every operationId checked against the contract
---

# autonomous-solutions-deposit-and-check-balance

Deposit funds into a user's wallet and verify the updated balance.

## Steps

1. 1. Call `create_wallet_deposit_users_wallet_deposit_post` with the required body fields (e.g., `amount`, `currency`).
2. 2. Call `get_wallet_balance_users_wallet_balance_get` to retrieve the wallet's current balance.

## Rules

- Include the authentication token in the `Authorization` header for each request.
- Respect the rate limit of 360 requests per minute; exceeding it returns HTTP 429.
