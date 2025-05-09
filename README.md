# OpenStreetMap API OpenAPI Specification

This repository contains an OpenAPI 3.0 specification for the OpenStreetMap API, focusing on the user endpoints. I do not plan to document all of the API endpoints, especially those that are used for moderating.

## Overview

The OpenStreetMap API allows developers to interact with OpenStreetMap data programmatically. This OpenAPI specification documents the API structure in a standardized format that can be used with various API tools and code generators.

## Contents

- `swagger.yaml` - The main OpenAPI specification file describing the OpenStreetMap API endpoints

## Features Documented

- User information retrieval by ID
- Authenticated user details retrieval
- Complete schema definitions for OSM user data including:
  - User attributes (ID, display name, account creation date)
  - User roles (moderator status)
  - Changeset and trace counts
  - Block information (received and issued)
  - Profile images

## Usage

### Viewing the Documentation

You can use any OpenAPI viewer to explore this specification. Some options include:

- [Swagger UI](https://swagger.io/tools/swagger-ui/)
- [Redoc](https://github.com/Redocly/redoc)
- [Stoplight Studio](https://stoplight.io/studio/)

Example with Swagger UI:

```bash
npx swagger-ui-dist/serve swagger.yaml
```

### Code Generation

You can use OpenAPI code generators to create client libraries in various programming languages:

```bash
# Using OpenAPI Generator
npx @openapitools/openapi-generator-cli generate -i swagger.yaml -g javascript -o ./generated-client
```

## Authentication

The OpenStreetMap API uses OAuth 2.0 for authentication. The specification includes the necessary security scheme definitions to work with the OSM OAuth system.

## License

This OpenAPI specification is licensed under [ODbL](https://opendatacommons.org/licenses/odbl/), the same license used by OpenStreetMap.

## Contributing

Contributions to improve the OpenAPI specification are welcome. Please feel free to submit issues or pull requests.
