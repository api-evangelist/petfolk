# Petfolk

Petfolk is a Charlotte, North Carolina based veterinary care company operating modern, company-owned
pet care centers across the US Southeast and Texas, paired with a consumer iOS/Android app for
booking, 24/7 care-team messaging, medication requests and pet medical records. Founded and led by
veterinarian Dr. Audrey Wystrach; raised a $40M Series B in October 2023 led by Movendo Capital.

## API posture

Petfolk is a consumer veterinary services operator, **not an API provider**. As of the 2026-08-02
enrichment pass there is no public developer portal, no API documentation, no OpenAPI / GraphQL /
AsyncAPI contract, no SDKs or packages on any public registry, no MCP server and no A2A agent card.
Contract discovery was run against `petfolk.com` (site root and `/api*`, `/graphql`, `/openapi.json`,
`/swagger.json`, `/api-docs`, `/docs`, `/redoc`) and against the `api.`, `developer.`, `docs.`,
`app.`, `status.` and `trust.` subdomains — all miss or do not resolve.

What Petfolk *does* publish that is machine-readable:

- **`llms.txt`** — a hand-authored agent-facing site map at <https://petfolk.com/llms.txt>
  (`llms/petfolk-llms.txt`). This is the company's only agent surface.
- **Mobile app association files** — Apple universal links and Android app links under
  `/.well-known/` (`well-known/`). Note: the Apple `apple-app-site-association` document is
  **malformed JSON** (trailing comma), which will break universal-link association.

## Artifacts

| Dir | File | Method |
|---|---|---|
| `llms/` | `petfolk-llms.txt` | searched (verbatim) |
| `well-known/` | `petfolk-well-known.yml`, `petfolk-apple-app-site-association.json`, `petfolk-assetlinks.json` | probed |
| `security/` | `petfolk-domain-security.yml` | probed |

## Links

- <https://petfolk.com/>
- <https://forgeglobal.com/petfolk_stock/> (secondary-market listing — harvest source)
