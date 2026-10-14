# checkmate

Audits an Auth0 tenant against security best practices and produces a report.

- **Upstream:** [`@auth0/auth0-checkmate`](https://github.com/auth0/auth0-checkmate) (npm)
- **Install type:** npm (run on demand through the pinned `npx` spec)

## Usage

```sh
auth0 plugins install checkmate
auth0 checkmate
```

When launched by the Auth0 CLI, checkmate reaches the Management API through the
CLI's local auth-injecting proxy, so it never handles a raw access token.

## Required scopes

The scopes listed in `plugin.json` are the read scopes checkmate needs to audit
a tenant. The CLI compares them against the active session and re-authenticates
for any that are missing before running the plugin.
