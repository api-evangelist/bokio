---
name: Connect a Bokio company via OAuth (public integration)
description: Run the OAuth 2.0 Authorization Code flow to obtain a company-scoped access token and manage connections.
api: openapi/bokio-general-api-openapi.yml
operations: [authorize, request-token, get-connections, delete-connection-by-id]
---

# Connect a Bokio company via OAuth (public integration)

Public integrations obtain a company-scoped token through the Bokio General API
OAuth 2.0 Authorization Code grant. Base URL `https://api.bokio.se/v1`.

## Prerequisites
- Registered `client_id` / `client_secret` and a registered `redirect_uri`.

## Steps
1. **Authorize** — `authorize`
   Redirect the user to `GET /authorize?client_id=...&redirect_uri=...&scope=<space-delimited>&state=<random>&response_type=code`.
   The `state` parameter is **required** (Bokio modification of RFC 6749) and
   must be validated on return to prevent CSRF. The authorization code expires
   in 5 minutes.
2. **Exchange for a token** — `request-token`
   `POST /token` with `Authorization: Basic base64(client_id:client_secret)`,
   `Content-Type: application/x-www-form-urlencoded`, body
   `grant_type=authorization_code&code=<code>`. Response includes
   `tenant_id`, `tenant_type`, `access_token` (bearer, 1-hour TTL) and a
   refresh token.
3. **Refresh** — `request-token`
   Reuse `POST /token` with `grant_type=refresh_token` before the access token
   expires.
4. **List / revoke connections** — `get-connections`, `delete-connection-by-id`
   `GET /connections` (filter with `tenantId`); `DELETE /connections/{connectionId}`
   removes tokens and company permissions (data created via the integration is
   retained).

## Rules
- Scopes are space-delimited (e.g. `journal-entries:read invoices:write`).
- Elevated scopes (e.g. `bank-payments:write`) require a partnership contract
  and Bokio approval. See `scopes/bokio-scopes.yml`.
