
# Getting Started

## Base URL

Replace the placeholder below with the public URL
assigned to your deployed FastAPI service.

```text
https://YOUR-API.onrender.com
```

## Your first request

To retrieve information about the Alpine A110, make
this request:

```http
GET /cars/Alpine/A110
```

The complete URL is:

```text
https://YOUR-API.onrender.com/cars/Alpine/A110
```

## Using Python

Install the requests package:

```bash
pip install requests
```

Then run:

```python
import requests

BASE_URL = "https://YOUR-API.onrender.com"

response = requests.get(
    f"{BASE_URL}/cars/Alpine/A110",
    timeout=15
)

response.raise_for_status()
print(response.json())
```

## Response format

A successful response contains the make and model
as JSON fields.

```json
{
  "make": "Alpine",
  "model": "A110"
}
```

## Interactive API documentation

Your FastAPI service also provides interactive
documentation at:

`https://YOUR-API.onrender.com/docs`
