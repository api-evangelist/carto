# CARTO GraphQL Schema

## Overview

This conceptual GraphQL schema models the CARTO location intelligence and spatial analytics platform. CARTO exposes REST APIs for Maps, SQL analytics, Workflows, Data Import, Data Observatory, and Account management — all built around a cloud-native architecture that connects directly to modern data warehouses (BigQuery, Snowflake, Redshift, Databricks). The schema below represents these capabilities as GraphQL types and operations.

**Source:** https://docs.carto.com/apis/

## Coverage

The schema covers the following CARTO API surface areas:

- **Maps API** — vector tables, tilesets, tileset sources, raster/H3/quadbin tiles
- **SQL API** — spatial SQL execution, query results, GeoJSON responses
- **Workflows API** — spatial data pipeline execution and management
- **Import API** — file/URL ingestion for CSV, GeoJSON, Shapefile formats
- **Data Observatory** — curated third-party spatial dataset catalog
- **Accounts API** — users, organizations, OAuth clients, API keys

## Types Summary

| Category | Types |
|---|---|
| Datasets & Tables | Dataset, DatasetDetails, DatasetMeta, Schema, Column, ColumnType, Table, TableDetails, TableSchema |
| Geometry | Geometry, GeometryType, Point, LineString, Polygon, MultiPoint, MultiLineString, MultiPolygon, GeometryCollection, Coordinate, BoundingBox |
| Features & Collections | Feature, FeatureDetails, FeatureCollection |
| Maps & Layers | Map, MapDetails, MapLayer, Layer, LayerDetails, LayerType, LayerStyle, Visualization, VisualizationDetails |
| Analytics | AnalysisNode, Analysis, AnalysisType, SpatialQuery, SQLQuery, QueryResult |
| Tiles | TileSet, TileDetails, TileStyle, CartoCSS |
| Import | Import, ImportDetails, ImportStatus |
| Organization & Users | Organization, OrgDetails, User, UserDetails, UserRole, Permission |
| Authentication | CartoAuth, OAuth, APIKey, Token |
| Geocoding & Routing | Geocoding, GeocodeResult, Isoline, Routing, Route, RouteLeg, RouteStep |
| Data Observatory | DataObservatory |

**Total named types:** 68

## Schema File

See `carto-schema.graphql` for the full GraphQL SDL definition.

## Authentication

CARTO uses OAuth 2.0 access tokens and API access tokens. All API requests require a valid `Authorization: Bearer <token>` header. Tokens are issued via the Accounts API at `https://accounts.app.carto.com`.

## Base URLs

- Maps / SQL / Workflows / Import: `https://gcp-us-east1.api.carto.com`
- Accounts: `https://accounts.app.carto.com`

## References

- CARTO Developer Portal: https://docs.carto.com/carto-for-developers
- Maps API Reference: https://docs.carto.com/carto-for-developers/reference/maps-api-reference
- SQL API Reference: https://docs.carto.com/carto-for-developers/reference/sql-api-reference
- Workflows API Reference: https://docs.carto.com/carto-for-developers/reference/workflows-api-reference
- Import API Reference: https://docs.carto.com/carto-for-developers/reference/import-api-reference
- Accounts API Reference: https://docs.carto.com/carto-for-developers/reference/accounts-api-reference
- Data Observatory: https://docs.carto.com/data-observatory
- Authorization: https://docs.carto.com/carto-for-developers/fundamentals/authorization
