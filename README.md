# 6K

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

6K Inc is a North Andover, Massachusetts advanced-materials company that produces engineered
powders and battery materials with **UniMelt**, its patented microwave-based production-scale
plasma system. Named for the ~6,000 K plasma temperature it operates at — the temperature of the
surface of the sun — UniMelt melts or vaporizes precursor feedstock into particles with precise
size distribution and crystalline phase in seconds, cutting energy use and eliminating wastewater
versus conventional processing.

- **6K Additive** (Burgettstown, PA) — sustainably sourced metal powders for additive
  manufacturing (Ti-6Al-4V, Ni625, Ni718, SS316L, tungsten, C103, C18150, HEA1000), reclaimed
  from CNC scrap and revert metal.
- **6K Energy** — domestically produced lithium-ion cathode and solid-state battery materials
  (NMC, LFP, LLZO, LMO, LTO, LNMO).

Applications span additive manufacturing, batteries, federal/defense, semiconductor CMP,
specialty ceramics, advanced coatings, lighting and display materials, and nano-engineered
powders. 6K has received US Department of Defense and Department of Energy awards for domestic
critical-materials capacity. Privately held; shares trade on secondary markets.

- https://www.6kinc.com/
- https://forgeglobal.com/6k_stock/ (secondary-market listing that surfaced this company)

## API surface — none

A full enrichment pass on **2026-07-31** ran STEP 0b contract discovery against every candidate
host and found **no machine-readable API contract and no developer program**:

| Surface | Result |
|---|---|
| OpenAPI / Swagger (`/openapi.json`, `/swagger.json`, `/api-docs`, `/docs`) | 404 |
| GraphQL | not found |
| MCP server | not found |
| A2A agent card (`/.well-known/agent-card.json` and `/.well-known/agent.json`) | 404 — **nothing written**, agent cards are search-only |
| AsyncAPI / webhooks | not found |
| `/.well-known/*` (security.txt, openid-configuration, oauth-authorization-server, api-catalog, ai-plugin.json) | all 404 |
| `llms.txt` | 404 (a generated one is saved to `llms/`) |
| `api.` / `docs.` / `developer.` / `status.` subdomains | wildcard DNS resolves them, but no HTTPS service answers |
| First-party SDKs / packages | none found on npm, PyPI or any registry |
| GitHub org | `github.com/6Kinc` exists but has 0 public repos and no linked website, so first-party ownership is unverified — **no `GitHubOrganization` pointer wired** |

The site's WordPress core REST API (`/wp-json/`) does answer 200. It is the CMS platform default,
not a product API 6K designs, documents or supports, so it is logged as an incidental finding in
`well-known/6k-well-known.yml` and deliberately **not** registered as an API — doing so would
misrepresent 6K as an API provider.

## Artifacts

| Path | Type | Method |
|---|---|---|
| `apis.yml` | APIs.json 0.20 index | searched |
| `security/6k-domain-security.yml` | DomainSecurity | probed |
| `well-known/6k-well-known.yml` | well-known + contract-discovery probe record (no pointer — nothing found) | probed |
| `llms/6k-llms.txt` | LLMsTxt | generated |

Vulnerability-disclosure and trust-center probes returned no verified hit, so those artifacts are
absent rather than empty.
