# Clojars

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

Community package repository for Clojure libraries with a REST API for searching artifacts, accessing version information, and managing deployment credentials.

**Base URL:** https://clojars.org/api  
**Documentation:** https://github.com/clojars/clojars-web/wiki/Data  
**Status:** https://clojars.statuspage.io  
**Maven Repository:** https://repo.clojars.org  

## APIs

| API | Description |
|-----|-------------|
| Clojars REST API | Search and retrieve Clojure artifact metadata, user profiles, group memberships, and release feeds |

## Key Endpoints

| Endpoint | URL |
|----------|-----|
| Get User | `GET /api/users/{username}` |
| Get Group Artifacts | `GET /api/groups/{group_name}` |
| Get Artifact | `GET /api/artifacts/{artifact_name}` |
| Get Artifact by Group | `GET /api/artifacts/{group_name}/{artifact_name}` |
| Release Feed | `GET /api/release-feed?from=yyyy-MM-ddTHH:mm:ssZ` |
| Search | `GET /search?q={query}&format=json` |
| All POMs | `GET /all-poms.txt` |
| All JARs | `GET /all-jars.clj` |
| Download Stats | `GET /stats/all.edn` |

## Authentication

Read endpoints are public and require no authentication. Publishing artifacts requires a free account and a deploy token created at https://clojars.org/tokens.

## Pricing

Clojars is free and open source. No paid plans or tiers exist. Funded by the [Clojurists Together Foundation](https://www.clojuriststogether.org/).

## Response Formats

Specify format via `Accept` header:

| Format | Content-Type |
|--------|--------------|
| JSON (default) | `application/json` |
| EDN | `application/edn` |
| YAML | `application/yaml` |
| Transit | `application/transit+json` |
