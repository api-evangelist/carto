# CARTO (carto)

CARTO is a cloud-native location intelligence platform that lets developers and analysts build spatial applications directly on top of modern data warehouses (BigQuery, Snowflake, Redshift, Databricks). It exposes a Maps API for vector and tileset map data, an SQL API for spatial analytics, a Workflows API for executing no-code spatial pipelines, an Import API for data ingestion, and the Data Observatory for curated third-party spatial datasets — all backed by OAuth access tokens and API access tokens.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/carto/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

 - Location Intelligence, Geospatial, Mapping, GIS, SQL, BigQuery, Snowflake, Data Warehouse

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-04-23

## APIs

### CARTO Maps API

Serves vector tables, SQL-query-backed tilesets, tileset sources, and raster/H3/quadbin tilesets for visualization in deck.gl, MapLibre, Google Maps, Amazon Location, or Mapbox GL clients.

**Human URL:** [Maps API Reference](https://docs.carto.com/carto-for-developers/reference/maps-api-reference)

#### Tags

 - Maps, Tiles, Vector, Geospatial

### CARTO SQL API

Executes SQL (including CARTO's spatial functions and analytics extensions) against a connected data warehouse from applications, returning GeoJSON / JSON results for spatial analysis, scoring, and dashboarding.

**Human URL:** [SQL API Reference](https://docs.carto.com/carto-for-developers/reference/sql-api-reference)

#### Tags

 - SQL, Analytics, Spatial

### CARTO Workflows API

Executes visually-designed CARTO Workflows (spatial data pipelines) programmatically, enabling scheduled, CI-driven, or application-triggered spatial analytics runs.

**Human URL:** [Workflows API Reference](https://docs.carto.com/carto-for-developers/reference/workflows-api-reference)

#### Tags

 - Workflows, Analytics, Automation

### CARTO Import API

Ingests files and URLs (CSV, GeoJSON, Shapefile, etc.) into a user's connected CARTO data warehouse for downstream spatial analysis and mapping.

**Human URL:** [Import API Reference](https://docs.carto.com/carto-for-developers/reference/import-api-reference)

#### Tags

 - Import, Ingestion, Data

### CARTO Data Observatory

Curated catalog of third-party spatial datasets (demographics, POIs, mobility, financial, environmental) accessible via subscription and queryable directly from the customer's cloud data warehouse.

**Human URL:** [Data Observatory](https://docs.carto.com/data-observatory)

#### Tags

 - Data Catalog, Datasets, Third-Party Data

### CARTO Accounts API

Manages CARTO user accounts, organizations, and API access tokens, including OAuth clients used for secure programmatic access.

**Human URL:** [Accounts API Reference](https://docs.carto.com/carto-for-developers/reference/accounts-api-reference)

#### Tags

 - Accounts, Authentication, OAuth

### CARTO for deck.gl

Client library providing deck.gl layers for CARTO vector, H3, quadbin, raster, and query sources, simplifying application-layer integration with the Maps API.

**Human URL:** [CARTO for deck.gl](https://docs.carto.com/carto-for-developers/carto-for-deck.gl)

#### Tags

 - SDK, deck.gl, Client Library

### CARTO for React

React library of components and hooks for building CARTO-powered location intelligence applications with widgets, filters, and deck.gl map integration.

**Human URL:** [CARTO for React](https://docs.carto.com/carto-for-developers/carto-for-react)

#### Tags

 - SDK, React, Client Library

## Use Cases

- Site selection and retail footfall analytics — combining Data Observatory demographics and POIs with retailer first-party data in BigQuery or Snowflake, then analyzing via the SQL API.
- Logistics and mobility — aggregating trip data into H3 or quadbin tilesets and serving low-latency vector tiles through the Maps API to an internal web app.
- Geospatial ETL — scheduling a CARTO Workflow (joining boundaries, enriching with Data Observatory, writing tilesets) from CI or a product back-end using the Workflows API.
- Data ingestion — uploading CSV, GeoJSON, or Shapefile datasets to the customer's connected warehouse via the Import API for downstream spatial analysis.
- Embedded dashboards — integrating CARTO for React widgets (formula, histogram, scatter, time-series, table) and deck.gl-powered maps into a customer-facing SaaS product.
- Insurance risk modeling — overlaying perils, boundaries, and exposure datasets with spatial SQL on BigQuery or Snowflake without moving data out of the warehouse.
- Telecom and infrastructure planning — raster and H3 analytics for coverage, capacity, and build-out planning.

## Common Properties

- [Website](https://carto.com)
- [Documentation Portal](https://docs.carto.com/)
- [CARTO for Developers](https://docs.carto.com/carto-for-developers)
- [Getting Started](https://docs.carto.com/getting-started/quickstart-guides)
- [Authentication](https://docs.carto.com/carto-for-developers/fundamentals/authorization)
- [FAQ](https://docs.carto.com/faqs)
- [What's New](https://docs.carto.com/whats-new)
- [Glossary](https://carto.com/glossary)
- [Webinars](https://carto.com/webinars)
- [Blog](https://carto.com/blog)
- [Partners](https://carto.com/partners)
- [Pricing](https://carto.com/pricing)
- [Support](https://docs.carto.com/faqs/support-packages)
- [Status](https://status.carto.com)
- [Login](https://auth.carto.com/u/login)
- [SignUp](https://auth.carto.com/u/signup)
- [TermsOfService](https://carto.com/legal)
- [PrivacyPolicy](https://carto.com/privacy)
- [GitHub Org](https://github.com/CartoDB)
- [JSON-LD Context](json-ld/carto-context.jsonld)
- [Vocabulary Definition](vocabulary.yml)
- [Spectral Rules](spectral/carto.spectral.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
