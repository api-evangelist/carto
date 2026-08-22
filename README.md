# Carto (carto)

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

CARTO is a cloud-native location intelligence platform that lets developers and analysts build spatial applications directly on top of modern data warehouses (BigQuery, Snowflake, Redshift, Databricks). It exposes a Maps API for vector and tileset map data, an SQL API for spatial analytics, a Workflows API for executing no-code spatial pipelines, an Import API for data ingestion, and the Data Observatory for curated third-party spatial datasets — all backed by OAuth access tokens and API access tokens.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/carto/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/carto/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- Location Intelligence
- Geospatial
- Mapping
- GIS
- SQL
- BigQuery
- Snowflake
- Data Warehouse

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-05-19

## APIs

### CARTO Maps API

Serves vector tables, SQL-query-backed tilesets, tileset sources, and raster/H3/quadbin tilesets for visualization in deck.gl, MapLibre, Google Maps, Amazon Location, or Mapbox GL clients.

- **Human URL:** [https://docs.carto.com/carto-for-developers/reference/maps-api-reference](https://docs.carto.com/carto-for-developers/reference/maps-api-reference)
- **Base URL:** `https://gcp-us-east1.api.carto.com`

#### Tags

- Maps
- Tiles
- Vector
- Geospatial

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/reference/maps-api-reference)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO SQL API

Executes SQL (including CARTO's spatial functions and analytics extensions) against a connected data warehouse from applications, returning GeoJSON / JSON results for spatial analysis, scoring, and dashboarding.

- **Human URL:** [https://docs.carto.com/carto-for-developers/reference/sql-api-reference](https://docs.carto.com/carto-for-developers/reference/sql-api-reference)
- **Base URL:** `https://gcp-us-east1.api.carto.com`

#### Tags

- SQL
- Analytics
- Spatial

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/reference/sql-api-reference)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO Workflows API

Executes visually-designed CARTO Workflows (spatial data pipelines) programmatically, enabling scheduled, CI-driven, or application- triggered spatial analytics runs.

- **Human URL:** [https://docs.carto.com/carto-for-developers/reference/workflows-api-reference](https://docs.carto.com/carto-for-developers/reference/workflows-api-reference)
- **Base URL:** `https://gcp-us-east1.api.carto.com`

#### Tags

- Workflows
- Analytics
- Automation

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/reference/workflows-api-reference)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO Import API

Ingests files and URLs (CSV, GeoJSON, Shapefile, etc.) into a user's connected CARTO data warehouse for downstream spatial analysis and mapping.

- **Human URL:** [https://docs.carto.com/carto-for-developers/reference/import-api-reference](https://docs.carto.com/carto-for-developers/reference/import-api-reference)
- **Base URL:** `https://gcp-us-east1.api.carto.com`

#### Tags

- Import
- Ingestion
- Data

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/reference/import-api-reference)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO Data Observatory

Curated catalog of third-party spatial datasets (demographics, POIs, mobility, financial, environmental) accessible via subscription and queryable directly from the customer's cloud data warehouse.

- **Human URL:** [https://docs.carto.com/data-observatory](https://docs.carto.com/data-observatory)

#### Tags

- Data Catalog
- Datasets
- Third-Party Data

#### Properties

- [Documentation](https://docs.carto.com/data-observatory)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO Accounts API

Manages CARTO user accounts, organizations, and API access tokens, including OAuth clients used for secure programmatic access.

- **Human URL:** [https://docs.carto.com/carto-for-developers/reference/accounts-api-reference](https://docs.carto.com/carto-for-developers/reference/accounts-api-reference)
- **Base URL:** `https://accounts.app.carto.com`

#### Tags

- Accounts
- Authentication
- OAuth

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/reference/accounts-api-reference)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO for deck.gl

Client library providing deck.gl layers for CARTO vector, H3, quadbin, raster, and query sources, simplifying application-layer integration with the Maps API.

- **Human URL:** [https://docs.carto.com/carto-for-developers/carto-for-deck.gl](https://docs.carto.com/carto-for-developers/carto-for-deck.gl)

#### Tags

- SDK
- deck.gl
- Client Library

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/carto-for-deck.gl)
- [Repository](https://github.com/CartoDB/deck.gl)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CARTO for React

React library of components and hooks for building CARTO-powered location intelligence applications with widgets, filters, and deck.gl map integration.

- **Human URL:** [https://docs.carto.com/carto-for-developers/carto-for-react](https://docs.carto.com/carto-for-developers/carto-for-react)

#### Tags

- SDK
- React
- Client Library

#### Properties

- [Documentation](https://docs.carto.com/carto-for-developers/carto-for-react)
- [Postman Collection](collections/carto.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/carto.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/carto)
- [Website](https://carto.com)
- [Portal](https://docs.carto.com/)
- [Developer](https://docs.carto.com/carto-for-developers)
- [Getting Started](https://docs.carto.com/getting-started/quickstart-guides)
- [Authentication](https://docs.carto.com/carto-for-developers/fundamentals/authorization)
- [F A Q](https://docs.carto.com/faqs)
- [Whats New](https://docs.carto.com/whats-new)
- [Glossary](https://carto.com/glossary)
- [Webinars](https://carto.com/webinars)
- [Blog](https://carto.com/blog)
- [Partners](https://carto.com/partners)
- [Pricing](https://carto.com/pricing)
- [Support](https://docs.carto.com/faqs/support-packages)
- [Status Page](https://status.carto.com)
- [Login](https://auth.carto.com/u/login)
- [Sign Up](https://auth.carto.com/u/signup)
- [Terms of Service](https://carto.com/legal)
- [Privacy Policy](https://carto.com/privacy)
- [Git Hub Org](https://github.com/CartoDB)
- [Integrations](https://carto.com/integrations/index.html)
- [M C P Server](https://carto.com/blog/carto-mcp-server-turn-your-ai-agents-into-geospatial-experts/)
- [L L Ms Txt](https://docs.carto.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
