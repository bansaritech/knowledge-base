# API Endpoints

Detailed documentation for all available API endpoints.

---

## Users

### List Users

Retrieve a paginated list of users.

```
GET /users
```

**Parameters:**

| Name | Type | In | Description |
|------|------|-----|-------------|
| `page` | integer | query | Page number (default: 1) |
| `limit` | integer | query | Items per page (default: 20) |
| `status` | string | query | Filter by status: `active`, `inactive` |

**Example Request:**

```bash
curl -X GET "https://api.example.com/v1/users?page=1&limit=10" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

**Example Response:**

```json
{
  "status": "success",
  "data": [
    {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com",
      "status": "active",
      "created_at": "2024-01-15T10:30:00Z"
    },
    {
      "id": 2,
      "name": "Jane Smith",
      "email": "jane@example.com",
      "status": "active",
      "created_at": "2024-01-16T14:20:00Z"
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 10,
    "total_items": 42,
    "total_pages": 5
  }
}
```

---

### Get User

Retrieve a single user by ID.

```
GET /users/{id}
```

**Parameters:**

| Name | Type | In | Description |
|------|------|-----|-------------|
| `id` | integer | path | **Required.** User ID |

**Example Request:**

```bash
curl -X GET "https://api.example.com/v1/users/123" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

**Example Response:**

```json
{
  "status": "success",
  "data": {
    "id": 123,
    "name": "John Doe",
    "email": "john@example.com",
    "status": "active",
    "role": "admin",
    "created_at": "2024-01-15T10:30:00Z",
    "updated_at": "2024-01-20T08:15:00Z"
  }
}
```

---

### Create User

Create a new user.

```
POST /users
```

**Request Body:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | User's full name |
| `email` | string | Yes | Unique email address |
| `password` | string | Yes | Min 8 characters |
| `role` | string | No | `user` (default), `admin` |

**Example Request:**

```bash
curl -X POST "https://api.example.com/v1/users" \
     -H "Authorization: Bearer YOUR_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{
       "name": "New User",
       "email": "newuser@example.com",
       "password": "securepassword123",
       "role": "user"
     }'
```

**Example Response:**

```json
{
  "status": "success",
  "data": {
    "id": 124,
    "name": "New User",
    "email": "newuser@example.com",
    "status": "active",
    "role": "user",
    "created_at": "2024-01-25T09:00:00Z"
  }
}
```

---

### Update User

Update an existing user.

```
PUT /users/{id}
```

**Parameters:**

| Name | Type | In | Description |
|------|------|-----|-------------|
| `id` | integer | path | **Required.** User ID |

**Request Body:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | User's full name |
| `email` | string | No | Unique email address |
| `status` | string | No | `active`, `inactive` |

**Example Request:**

```bash
curl -X PUT "https://api.example.com/v1/users/123" \
     -H "Authorization: Bearer YOUR_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{
       "name": "John Updated",
       "status": "inactive"
     }'
```

---

### Delete User

Delete a user.

```
DELETE /users/{id}
```

**Example Request:**

```bash
curl -X DELETE "https://api.example.com/v1/users/123" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

**Response:** `204 No Content`

---

## Products

### List Products

```
GET /products
```

**Parameters:**

| Name | Type | In | Description |
|------|------|-----|-------------|
| `category` | string | query | Filter by category |
| `min_price` | number | query | Minimum price |
| `max_price` | number | query | Maximum price |
| `in_stock` | boolean | query | Filter by availability |

**Example Response:**

```json
{
  "status": "success",
  "data": [
    {
      "id": 1,
      "name": "Widget Pro",
      "description": "A professional widget",
      "price": 29.99,
      "category": "electronics",
      "in_stock": true,
      "quantity": 150
    }
  ]
}
```

---

### Get Product

```
GET /products/{id}
```

---

### Create Product

```
POST /products
```

**Request Body:**

```json
{
  "name": "New Product",
  "description": "Product description",
  "price": 19.99,
  "category": "electronics",
  "quantity": 100
}
```

---

## Orders

### List Orders

```
GET /orders
```

### Get Order

```
GET /orders/{id}
```

### Create Order

```
POST /orders
```

**Request Body:**

```json
{
  "user_id": 123,
  "items": [
    {
      "product_id": 1,
      "quantity": 2
    },
    {
      "product_id": 5,
      "quantity": 1
    }
  ],
  "shipping_address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA",
    "zip": "12345",
    "country": "US"
  }
}
```

---

## Error Codes

| Code | Description |
|------|-------------|
| `INVALID_REQUEST` | Request body validation failed |
| `RESOURCE_NOT_FOUND` | Requested resource doesn't exist |
| `DUPLICATE_ENTRY` | Resource already exists (e.g., email) |
| `RATE_LIMIT_EXCEEDED` | Too many requests |
| `UNAUTHORIZED` | Invalid or missing API key |
| `FORBIDDEN` | Not authorized for this action |
| `INTERNAL_ERROR` | Server-side error |

---

## Webhooks

Configure webhooks to receive real-time notifications:

```
POST /webhooks
```

**Supported Events:**

- `user.created`
- `user.updated`
- `user.deleted`
- `order.created`
- `order.completed`
- `order.cancelled`

**Webhook Payload:**

```json
{
  "event": "order.created",
  "timestamp": "2024-01-25T10:00:00Z",
  "data": {
    "id": 456,
    "user_id": 123,
    "total": 59.98
  }
}
```
