
# Getting Started

## Base URL

Base URL

```text
https://car-api-oos.onrender.com
```

## Your first request

To retrieve information about the Alpine A110, make
this request:

```http
GET /cars/Alpine/A110
```

The complete URL is:

```text
https://car-api-oos.onrender.com
```

## Using Python

Install the requests package:

```bash
pip install requests
```

Then run:

```python
import requests

BASE_URL = "https://car-api-oos.onrender.com"

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


