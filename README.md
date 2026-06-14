# Clojars

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
