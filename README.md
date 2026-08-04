# Petfolk

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
