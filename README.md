# Seoul National University (snu)

Seoul National University (SNU) is South Korea's flagship national research university and is ranked #34 in the QS World University Rankings 2025. This repository catalogs SNU's public, machine-readable developer/API footprint as an APIs.json profile. The primary confirmed public API is the S-Space OAI-PMH interface — the SNU Open Repository and Archive, a DSpace institutional repository.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/snu/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=snu-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

- Education
- Higher Education
- University
- Research
- Open Access
- Institutional Repository
- OAI-PMH
- South Korea

## APIs

- **S-Space OAI-PMH Repository Interface** — OAI-PMH 2.0 metadata harvesting for the SNU Open Repository and Archive (DSpace). Verified live.
  - Docs: https://s-space.snu.ac.kr/
  - Base URL: https://s-space.snu.ac.kr/oai/request
  - Identify: https://s-space.snu.ac.kr/oai/request?verb=Identify
  - Metadata formats: https://s-space.snu.ac.kr/oai/request?verb=ListMetadataFormats

## Plans

- [plans/snu-plans-pricing.yml](plans/snu-plans-pricing.yml)

## Rate Limits

- [rate-limits/snu-rate-limits.yml](rate-limits/snu-rate-limits.yml)

## FinOps

- [finops/snu-finops.yml](finops/snu-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://en.snu.ac.kr/
- LinkedIn: https://www.linkedin.com/school/seoulnational-university
- Plans: plans/snu-plans-pricing.yml
- Rate Limits: rate-limits/snu-rate-limits.yml
- FinOps: finops/snu-finops.yml
- Review: review.yml

## Notes

- Only confirmed, public URLs are cataloged; no endpoints were fabricated.
- The S-Space OAI-PMH endpoint was verified live (HTTP 200) with a valid OAI-PMH 2.0 Identify response.
- The DSpace REST API (`/server/api`, `/rest`) is present but returned HTTP 403 to scripted access, so it is not cataloged as a usable public API.
- No centralized developer portal, general-purpose open-data API, or official unified SNU GitHub organization was found (only lab-level GitHub orgs exist), so no `GitHub` common property is listed.

## Maintainers

- Kin Lane — kin@apievangelist.com
