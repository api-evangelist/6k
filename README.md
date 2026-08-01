# 6K

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
