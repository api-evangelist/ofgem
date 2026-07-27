# Ofgem (ofgem)

Ofgem, the Office of Gas and Electricity Markets, is the non-ministerial government department that regulates the gas and electricity markets of Great Britain (England, Scotland and Wales), drawing its powers from the Gas Act 1986, the Electricity Act 1989 and the Energy Act 2023. It licenses the companies that make, transport and sell energy, sets the price cap, runs the RIIO network price controls, administers environmental and social schemes such as the Renewables Obligation, REGO and Feed-in Tariffs on behalf of government, grants and supervises the Smart Meter Communication Licence held by the Smart DCC, and imposes the Data Best Practice licence obligation that requires network licensees to treat Energy System Data as presumed open. It sits above the value chain rather than in it — it holds no customers, no meters and no wires. Its own API posture is the plain finding: Ofgem publishes no API of any kind. There is no developer portal, no `api.`, `docs.`, `data.` or `developer.` subdomain, no OpenAPI, no CKAN endpoint. Market data is genuinely open but delivered as chart images, CSV and XLSX file downloads from the Ofgem Data Portal; consumer data does not exist here at all, because Great Britain mandated the smart-meter infrastructure rather than a consumer data right, and no CDR-equivalent obligation binds either Ofgem or the suppliers it licenses. Ofgem's two operational registers — the Electronic Public Register and the Renewable Electricity Register — are login-gated applications whose backends are undocumented and unpublished. Ofgem is therefore a regulator that demands open, discoverable, interoperable data from the industry it supervises while shipping none of it programmatically itself.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ofgem/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ofgem/refs/heads/main/apis.yml)

## Tags

- Energy
- United Kingdom
- Utilities
- Electricity
- Gas
- Energy Markets
- Regulator
- Smart Metering
- Open Data
- Energy Regulation
- Renewables
- Great Britain

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

None. Ofgem publishes no documented public API.

Every developer-facing host was probed on 2026-07-27 and none resolves: `api.ofgem.gov.uk`, `developer.ofgem.gov.uk`, `developers.ofgem.gov.uk`, `docs.ofgem.gov.uk`, `data.ofgem.gov.uk`, `portal.ofgem.gov.uk`, `open.ofgem.gov.uk`, `opendata.ofgem.gov.uk`, `dsi.ofgem.gov.uk`, `dataexchange.ofgem.gov.uk`. Every developer-facing path on the main site returns 404, including `/developers`, `/api`, `/data`, `/openapi.json`, `/swagger.json`, `/jsonapi`, `/graphql` and `/llms.txt`. No OpenAPI, AsyncAPI, GraphQL schema or Postman collection exists to harvest, so no `openapi/` directory is present in this repo.

## Mandate posture

| | |
|---|---|
| **Mandate regime** | `smart-meter-infrastructure` — Ofgem grants and regulates the Smart Meter Communication Licence held by Smart DCC Ltd and oversees the Smart Energy Code. Ofgem administers this regime; it is not a data holder under it. |
| **Mandate status** | `live-implemented` — the regime and Ofgem's own licence-condition data obligations are in force and verified (Data Best Practice Guidance v1.0, November 2021, fetched at HTTP 200; live Electronic Public Register at HTTP 200). This says nothing about an API. Ofgem implemented no API. |
| **Consumer data right** | None. Great Britain has no CDR-energy, no Green Button regulation, no accredited-recipient scheme. DESNZ's energy smart data call for evidence (January 2025) under the Data (Use and Access) Act 2025 and Ofgem's Consumer Consent Decision (OFG1164, April 2025) are policy work, not endpoints. |
| **Data standard** | No standard reference found — no Green Button/ESPI, no CDR Consumer Data Standards, no IEC CIM, no IEEE 2030.5, no OpenADR, no OCPP/OCPI. |
| **Market data** | Open and anonymous, but as files. The Ofgem Data Portal publishes charts with PNG and CSV downloads across retail, wholesale, network and customer-service indicators; price cap levels and FIT installation reports are XLSX. |
| **Consumer data API** | None, and structurally so — a regulator holds no meters, no accounts and no consumption records. |
| **Access gate** | `none-published` — no developer portal, no key request, no application route, no accreditation, no data licence. The Data Exchange Service is the only Ofgem system that mentions an API and it is inbound-only, in Beta, and invitation-only (`ofgemdataservices@ofgem.gov.uk`). |
| **Auth model** | No public API to authenticate against. The Electronic Public Register uses OAuth 2.0 authorization code + PKCE via AWS Cognito; the Renewable Electricity Register uses OpenID Connect authorization code + PKCE via Azure AD B2C. No OIDC discovery document is served anywhere. |
| **Home market** | United Kingdom (Great Britain — England, Scotland, Wales). |

## The finding

Ofgem's Data Best Practice licence condition works — on everyone except Ofgem. The "presumed open" obligation Ofgem placed on RIIO-price-controlled licensees produced NESO's public CKAN API and the DNO open-data portals. The regulator that wrote the rule ships spreadsheets.

## Properties

- [Website](https://www.ofgem.gov.uk/)
- [About](https://www.ofgem.gov.uk/about-us)
- [Data Portal](https://www.ofgem.gov.uk/news-and-insight/data/data-portal)
- [Data](https://www.ofgem.gov.uk/news-and-insight/data)
- [Data release calendar](https://www.ofgem.gov.uk/data/ofgem-data-upcoming-release-calendar)
- [Digitalisation](https://www.ofgem.gov.uk/energy-regulation/technology-and-innovation/digitalisation)
- [Data Best Practice Guidance v1.0](https://www.ofgem.gov.uk/sites/default/files/2021-11/Data_Best_Practice_Guidance_v1.pdf)
- [Electronic Public Register](https://epr.ofgem.gov.uk/)
- [Renewable Electricity Register](https://rer.ofgem.gov.uk/)
- [Vulnerability disclosure](https://www.ofgem.gov.uk/report-vulnerability)
- [security.txt](https://www.ofgem.gov.uk/.well-known/security.txt)
- [News](https://www.ofgem.gov.uk/news-and-insight)
- [Blog](https://www.ofgem.gov.uk/blog)
- [RSS](https://www.ofgem.gov.uk/rss.xml)
- [Publications](https://www.ofgem.gov.uk/publications)
- [LinkedIn](https://www.linkedin.com/company/ofgem)

## Maintainers

- Kin Lane — kin@apievangelist.com
