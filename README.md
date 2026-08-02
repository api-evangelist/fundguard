# FundGuard

AI-powered, cloud-native investment accounting operating system for asset managers, asset owners, custodian banks and fund administrators — a single real-time accounting engine covering Fund Accounting/ABOR, Investment Accounting/IBOR and Private Markets portfolio accounting, with shadow and contingent NAV, reconciliation, Report Studio and AI-driven anomaly detection. Founded 2018; New York HQ with offices in Dedham MA, Tel Aviv and London.

- Website — https://www.fundguard.com/
- Product — https://www.fundguard.com/product/
- News — https://www.fundguard.com/news/
- Knowledge base (login required) — https://kb.fundguard.com/knowledge
- Secondary market — https://forgeglobal.com/fundguard_stock/

## API surface (as of 2026-08-01)

FundGuard markets an API-first platform but publishes **no public developer portal, API reference, OpenAPI/AsyncAPI/GraphQL contract, SDK or CLI**. Contract discovery was run against every host that resolves plus every name in certificate transparency — see `x-contract-discovery` in `apis.yml`.

The one publicly reachable machine-readable surface is a **Model Context Protocol server on the corporate web host**, advertised through RFC 8414 and RFC 9728 metadata:

- `https://www.fundguard.com/wp-json/mcp/mcp-oauth-server` — OAuth 2.1 (authorization_code + PKCE S256), scope `mcp`, `tools/list` returns 401 anonymously.

This is the WordPress-site MCP adapter, not the investment accounting platform API.

## Artifacts

| Dir | File | Method |
|---|---|---|
| `well-known/` | index + two verbatim OAuth metadata documents | searched |
| `mcp/` | `fundguard-mcp.yml` | probed |
| `authentication/` | `fundguard-authentication.yml` | probed |
| `scopes/` | `fundguard-scopes.yml` | probed |
| `conformance/` | `fundguard-conformance.yml` | searched |
| `lifecycle/` | `fundguard-lifecycle.yml` | searched |
| `security/` | `fundguard-domain-security.yml` | probed |
| `llms/` | `fundguard-llms.txt` | generated |

No A2A agent card, security.txt, vulnerability disclosure program, trust center, status page, changelog, SDK/package, CLI or sandbox was found. Those absences are recorded in the artifacts above rather than left blank.
