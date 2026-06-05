# Carto (carto)

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
