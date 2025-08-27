# API Reference (Reference Server)

Endpoints (minimal):
- `GET /collections` — list collections
- `GET /collections/addresses` — describe the addresses collection
- `GET /collections/addresses/items` — list address features (GeoJSON FeatureCollection)
- `GET /conformance` — list OGC API Features conformance classes

OpenAPI documentation:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`
- OpenAPI JSON: `http://localhost:8000/openapi.json`

Spec stubs (static):
- YAML: `specs/ogc-api-features.yml`
- JSON: `specs/ogc-api-features.json`

Run the reference server from `api-server` and test with QGIS or a web client.
