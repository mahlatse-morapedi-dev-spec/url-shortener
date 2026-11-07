# Request Lifecycle — LinkLite

## 1. URL Creation Lifecycle

### Incoming Request

The client sends:

`POST /api/v1/urls`

Request body:

```json
{
  "original_url": "https://example.com/products/123"
}
```

### Processing Steps

1. Django receives the HTTP request.
2. Django REST Framework resolves the URL route.
3. The API view receives the request.
4. The serializer validates the submitted URL.
5. The URL service checks whether the exact URL already exists.
6. If it exists, the existing mapping is returned.
7. Otherwise, a new short code is generated.
8. A database record is created.
9. The API returns HTTP 201 with the shortened URL.

### Response

The API returns the original URL, short code, shortened URL and timestamp.

## 2. URL Redirection Lifecycle

### Incoming Request

The visitor accesses:

`GET /aB92xK`

### Processing Steps

1. Django receives the request.
2. The URL router extracts the short code.
3. The redirect view retrieves the corresponding database record.
4. If no record exists, HTTP 404 is returned.
5. If the record exists, the original URL is retrieved.
6. Django returns HTTP 302 with the destination in the Location header.
7. The visitor's browser follows the redirect.

## 3. Failure Scenarios

| Failure | Expected Behaviour |
|---|---|
| Invalid URL | HTTP 400 |
| Empty URL | HTTP 400 |
| Unknown short code | HTTP 404 |
| Duplicate URL | Return existing mapping |
| Short-code collision | Generate another code |
| Database unavailable | Controlled HTTP 500 response |
| Unexpected internal exception | Log error and return safe response |
