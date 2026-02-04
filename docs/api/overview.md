# API Overview

This section demonstrates how to document an API using MkDocs.

## Introduction

The Example API provides programmatic access to our platform's features. This RESTful API uses JSON for request and response bodies.

## Base URL

All API requests should be made to:

```
https://api.example.com/v1
```

## Authentication

### API Key Authentication

Include your API key in the request header:

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" \
     https://api.example.com/v1/users
```

### Getting an API Key

1. Log in to your dashboard
2. Navigate to **Settings** > **API Keys**
3. Click **Generate New Key**
4. Copy and securely store your key

> **Warning:** Never share your API key or commit it to version control.

## Request Format

### Headers

| Header | Required | Description |
|--------|----------|-------------|
| `Authorization` | Yes | Bearer token for authentication |
| `Content-Type` | Yes* | `application/json` for POST/PUT |
| `Accept` | No | `application/json` (default) |

### Query Parameters

```
GET /users?page=1&limit=10&sort=created_at&order=desc
```

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `page` | integer | 1 | Page number |
| `limit` | integer | 20 | Items per page (max: 100) |
| `sort` | string | `id` | Field to sort by |
| `order` | string | `asc` | Sort order (`asc` or `desc`) |

## Response Format

### Success Response

```json
{
  "status": "success",
  "data": {
    "id": 123,
    "name": "Example"
  },
  "meta": {
    "request_id": "req_abc123"
  }
}
```

### Error Response

```json
{
  "status": "error",
  "error": {
    "code": "INVALID_REQUEST",
    "message": "The request body is invalid",
    "details": [
      {
        "field": "email",
        "message": "Invalid email format"
      }
    ]
  },
  "meta": {
    "request_id": "req_xyz789"
  }
}
```

## HTTP Status Codes

| Code | Status | Description |
|------|--------|-------------|
| 200 | OK | Request succeeded |
| 201 | Created | Resource created successfully |
| 204 | No Content | Request succeeded, no content returned |
| 400 | Bad Request | Invalid request format |
| 401 | Unauthorized | Missing or invalid authentication |
| 403 | Forbidden | Authenticated but not authorized |
| 404 | Not Found | Resource doesn't exist |
| 429 | Too Many Requests | Rate limit exceeded |
| 500 | Internal Server Error | Server error |

## Rate Limiting

API requests are limited to:

- **Free tier:** 100 requests per minute
- **Pro tier:** 1,000 requests per minute
- **Enterprise:** Unlimited

Rate limit headers are included in every response:

```
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 95
X-RateLimit-Reset: 1640000000
```

## Pagination

List endpoints return paginated results:

```json
{
  "data": [...],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total_items": 150,
    "total_pages": 8
  }
}
```

## Versioning

The API is versioned via URL path:

```
https://api.example.com/v1/...
https://api.example.com/v2/...
```

The current stable version is **v1**.

## SDKs and Libraries

Official SDKs are available for:

- [Python SDK](https://github.com/example/python-sdk)
- [JavaScript SDK](https://github.com/example/js-sdk)
- [Go SDK](https://github.com/example/go-sdk)

## Next Steps

- View the [API Endpoints](endpoints.md) documentation
- Try the API in our [Interactive Playground](https://api.example.com/playground)
