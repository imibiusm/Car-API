
# API Reference

All endpoints return JSON responses.

Replace `YOUR-API.onrender.com` with your actual API hostname.

## 1. Get a car

**Method:** `GET`

```text
/cars/{car_make}/{car_model}
```

Returns a specific car if the make and model exist.

Example:

```text
/cars/Alpine/A110
```

Successful response (`200 OK`):

```json
{
  "make": "Alpine",
  "model": "A110"
}
```

Possible error (`404 Not Found`):

```json
{
  "detail": "Make not found"
}
```

## 2. List car brands

**Method:** `GET`

```text
/brands
```

Returns the available manufacturers and their count.

Example response:

```json
{
  "count": 3,
  "brands": ["Abarth", "Alpine", "BMW"]
}
```

The actual count and brand list depend on the database.

## 3. List models for a brand

**Method:** `GET`

```text
/cars/{car_make}
```

Example:

```text
/cars/Alpine
```

Returns the selected brand and its models.

## 4. Search for models

**Method:** `GET`

```text
/search?q={search_term}
```

Example:

```text
/search?q=Spider
```

Returns models whose names contain the search term.

## 5. Random Car

**Method:** `GET`

```text
/random
```

Example:

```text
/random

```
```json
{
  "make": "MG",
  "model": "MG S9"
}
```

## 6. Stats

**Method:** `GET`

```text
/stats
```
{
  "total_makes": 236,
  "total_models": 4210
}

```json
{
  "make": "MG",
  "model": "MG S9"
}
```




## HTTP status codes

| Status | Meaning |
|---|---|
| `200` | Request succeeded |
| `404` | Route, brand or model not found |
| `422` | Request parameters failed validation |
| `500` | Unexpected server error |
