---
name: autonomous-solutions-create-and-retrieve-deal
description: Create a new deal and then retrieve its details.
api: openapi/autonomous-solutions-openapi.json
operations:
- create_deal_deals__post
- get_deal_by_id_deals__deal_id__get
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/autonomous-solutions-openapi.json ; every operationId checked against the contract
---

# autonomous-solutions-create-and-retrieve-deal

Create a new deal and then retrieve its details.

## Steps

1. 1. Call `create_deal_deals__post` with the required request body fields for a new deal.
2. 2. Call `get_deal_by_id_deals__deal_id__get` using the `deal_id` returned from the create operation.

## Rules

- Auth: Include the provider's required authentication token in the `Authorization` header for each request.
- Rate limit: Do not exceed 360 requests per minute; a 429 response indicates exhaustion.
