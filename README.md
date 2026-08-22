# Seoul National University (snu)

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

Seoul National University (SNU) is South Korea's flagship national research university, a national
university corporation identified by ROR as [04h9pn542](https://ror.org/04h9pn542). This repository
is an APIs.json profile of SNU's public, machine-readable footprint, built under the API Evangelist
**university pipeline** — which settles *who operates* each surface before saving any contract,
because a university is a federation of buyers rather than a producer of APIs.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/snu/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=snu-api-evangelist&utm_content=repo

## What SNU actually operates

SNU publishes **no developer portal, no API documentation, no open-data portal, no API gateway, no
official GitHub organization, and no OAuth or OIDC authorization server.** Every contract in this
repository was written from live probing on 2026-08-19, not from anything SNU wrote.

What it does run is four machine-readable surfaces, all on its own hosts and its own address block:

| Surface | Operator | Protocol | Status |
|---|---|---|---|
| [S-Space OAI-PMH](https://s-space.snu.ac.kr/oai/request?verb=Identify) | institution | OAI-PMH 2.0 | Open, anonymous, no challenge |
| [KOSSDA OAI-PMH](https://kossda.snu.ac.kr/oai/request?verb=Identify) | institution | OAI-PMH 2.0 | Open, but slow (needs a >45s read timeout) |
| [S-Space OpenSearch](https://s-space.snu.ac.kr/open-search/description.xml) | institution | OpenSearch 1.1 | **Gated** behind a JavaScript bot challenge |
| SNU SAML Identity Provider (`kafegw.snu.ac.kr`) | institution | SAML 2.0 | Live in KAFE / eduGAIN; metadata only via the federation |
| [SNU Library discovery](https://snu-primo.hosted.exlibrisgroup.com/primo-explore/search?vid=82SNU) | **tenant** | Ex Libris Primo / Alma | Real tenancy (82SNU) — Ex Libris's contract, not SNU's |

## Type

- University / Public Research University / Index / Consumer / 3rd-Party

## The operator axis

The last row is the point of this pipeline. SNU Library genuinely runs a discovery service, and
`snu-primo.hosted.exlibrisgroup.com` is genuinely SNU's — but the API, the contract and the
engineering are Ex Libris's. It is recorded here as `x-operator: tenant` and **no Ex Libris
specification is saved under this institution.** The tenancy is a real institutional fact; the
contract belongs to the vendor's own profile.

## The find

SNU operates a **SAML 2.0 Identity Provider** — entityID `https://kafegw.snu.ac.kr/idp/simplesamlphp`,
registered by the Korea Access Federation on 2024-06-25 and exported into eduGAIN, where exactly one
of 10,566 entities carries the `snu.ac.kr` scope. It supports REFEDS Research & Scholarship, asserts
Sirtfi with a published security contact, and holds signing and encryption certificates issued to
`O=SNU, OU=Information Systems and Technology` valid to 2028-06-03. Institution-operated by
definition and machine-readable by definition, and it had never been catalogued.

SNU does not serve its own metadata — the entityID URL 404s and the SimpleSAMLphp metadata path
returns 500 — so the eduGAIN aggregate is the only retrievable copy. It is mirrored to
[`authentication/snu-kafe-saml-idp-metadata.xml`](authentication/snu-kafe-saml-idp-metadata.xml).

## Corrections to the 2026-06-03 profile

- The DSpace REST API previously recorded as "present but HTTP 403" **does not exist.** The 403 was a
  JavaScript bot challenge, not an access control; behind the challenge cookie `/rest` and
  `/server/api` return 404 from a DSpace 5.5 error page. Absent, not gated.
- Three institution-operated surfaces were missing: KOSSDA, S-Space OpenSearch, and the SAML IdP.

## Read the negatives

`x-coverage` in [apis.yml](apis.yml) and the endpoint table in [review.yml](review.yml) record what
is *not* there with the status code that established it — `api.snu.ac.kr` is not a gateway (403 root,
404 everywhere), `data.snu.ac.kr` is a research lab's website and not an open-data portal, the LMS at
`etl.snu.ac.kr` is neither Moodle nor Canvas and exposes no LTI, `dcollection.snu.ac.kr` soft-404s on
every OAI path, and SNU is not a DataCite member (its repositories mint Handles, not DOIs).

## Domain standards (Kin Score `education` regime)

Conforms: `oai-pmh`, `saml`, `shibboleth` (metadata profile, via SimpleSAMLphp), plus OpenSearch 1.1.
Does not: `scim`, `lti`, `oneroster`, `ed-fi`, `caliper`, `qti`, `orcid`, `datacite`, `crossref` —
each with the negative probe recorded in [conformance/snu-conformance.yml](conformance/snu-conformance.yml).

## Artifacts

- [openapi/](openapi/) — three probed contracts (+ [`_original/`](openapi/_original/))
- [authentication/](authentication/) — SAML IdP metadata + the authentication summary
- [conformance/](conformance/) · [lifecycle/](lifecycle/) · [scopes/](scopes/) · [errors/](errors/)
- [vocabulary/](vocabulary/) · [json-schema/](json-schema/) · [json-ld/](json-ld/) · [rules/](rules/)
- [examples/](examples/) — six responses captured live from SNU's own hosts
- [plans/](plans/snu-plans-pricing.yml) · [rate-limits/](rate-limits/snu-rate-limits.yml) · [finops/](finops/snu-finops.yml) · [security/](security/snu-domain-security.yml)

## AI posture

- AI policy: [「서울대학교 AI 가이드라인」](https://www.snu.ac.kr/about/downloads?md=v&bbsidx=166508) (Korean surface)
- AI tooling: [SNU "AI Native Campus"](https://www.snu.ac.kr/snunow/press?md=v&bbsidx=170942) — ChatGPT Edu for all current students and staff, June 2026 to August 2027, authenticated with SNU Portal credentials

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-19

## Notes

- Only confirmed, public URLs are cataloged; no endpoints were fabricated and no vendor specification
  is saved under this institution.
- Every artifact carries `generated`, `method` and `source`. Every contract here is `method: probed`.

## Maintainers

- Kin Lane — kin@apievangelist.com
