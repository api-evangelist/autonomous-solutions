---
name: autonomous-solutions-create-and-get-user
description: Create a new user and then retrieve the created user's data.
api: openapi/autonomous-solutions-openapi.json
operations:
- create_user_users_user_post
- get_user_data_with_hub_users_user_get
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/autonomous-solutions-openapi.json ; every operationId checked against the contract
---

# autonomous-solutions-create-and-get-user

Create a new user and then retrieve the created user's data.

## Steps

1. 1. `create_user_users_user_post` – send a POST request to `/users/user` with the required JSON body fields for the new user.
2. 2. `get_user_data_with_hub_users_user_get` – send a GET request to `/users/user` (optionally include query parameters for hub selection) to fetch the newly created user's details.

## Rules

- Include the authentication token in the `Authorization` header for both requests.
- Respect the rate limit of 360 requests per minute; exceeding it returns HTTP 429.
