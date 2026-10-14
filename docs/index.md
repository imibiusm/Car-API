
# Car Database API

Welcome to the Car Database API documentation.

This API lets you look up car manufacturers and their models
using simple HTTP requests.

## Features

- Browse available car brands.
- Retrieve models for a manufacturer.
- Look up a specific car by make and model.
- Search model names.
- Receive JSON responses.

## Quick example

Request:

```http
GET /cars/Alpine/A110
```

Example response:

```json
{
  "make": "Alpine",
  "model": "A110"
}
```

## Explore the API

Use the links below to learn how to get started
and understand the available endpoints.

- [Getting Started](getting-started.md)
- [API Reference](endpoints.md)
