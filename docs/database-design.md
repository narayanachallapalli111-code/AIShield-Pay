# Database Design

Each microservice owns its own database.

## Payment Service

### payment

| Column | Type |
|---------|------|
| id | UUID |
| amount | DECIMAL |
| currency | VARCHAR |
| status | VARCHAR |
| payment_method | VARCHAR |
| created_at | TIMESTAMP |

---

## User Service

### users

| Column | Type |
|---------|------|
| id | UUID |
| first_name | VARCHAR |
| last_name | VARCHAR |
| email | VARCHAR |
| password | VARCHAR |

---

## Wallet Service

### wallet

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| balance | DECIMAL |

---

## Ledger Service

### ledger

| Column | Type |
|---------|------|
| id | UUID |
| payment_id | UUID |
| debit | DECIMAL |
| credit | DECIMAL |
| transaction_date | TIMESTAMP |

---

## Database Rules

- One database per microservice
- No shared tables
- UUID primary keys
- Audit fields in every table
- Soft delete where applicable