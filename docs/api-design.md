# API Design

## API Version

```
/api/v1
```

---

## Authentication APIs

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /auth/login | Login |
| POST | /auth/register | Register User |
| POST | /auth/refresh | Refresh Token |

---

## Payment APIs

| Method | Endpoint |
|---------|----------|
| POST | /payments |
| GET | /payments |
| GET | /payments/{id} |
| PUT | /payments/{id} |
| DELETE | /payments/{id} |

---

## Wallet APIs

| Method | Endpoint |
|---------|----------|
| GET | /wallets/{id} |
| POST | /wallets/deposit |
| POST | /wallets/withdraw |

---

## User APIs

| Method | Endpoint |
|---------|----------|
| POST | /users |
| GET | /users |
| GET | /users/{id} |
| PUT | /users/{id} |
| DELETE | /users/{id} |

---

## Standard HTTP Status Codes

| Code | Meaning |
|------|---------|
|200|Success|
|201|Created|
|400|Bad Request|
|401|Unauthorized|
|403|Forbidden|
|404|Not Found|
|409|Conflict|
|500|Internal Server Error|

---

## Response Format

```json
{
  "timestamp": "",
  "status": 200,
  "message": "Success",
  "data": {}
}
```

---

## Error Response

```json
{
  "timestamp": "",
  "status": 400,
  "error": "Validation Failed"
}
```