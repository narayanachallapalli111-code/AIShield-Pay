# Kafka Event Design

## Event Flow

```text
Payment Created
        |
        |
Payment Service
        |
        |
Kafka
        |
+-------+--------+
|       |        |
|       |        |
Ledger Notification Fraud
```

---

## Topics

| Topic |
|-------|
| payment-created |
| payment-success |
| payment-failed |
| notification-send |
| fraud-detected |

---

## PaymentCreatedEvent

```json
{
  "paymentId":"",
  "userId":"",
  "amount":1000,
  "currency":"INR",
  "status":"PENDING",
  "createdAt":""
}
```

---

## PaymentSuccessEvent

```json
{
  "paymentId":"",
  "status":"SUCCESS"
}
```

---

## PaymentFailedEvent

```json
{
  "paymentId":"",
  "reason":"INSUFFICIENT_FUNDS"
}
```

---

## Event Naming

Past tense.

Examples

- PaymentCreated
- PaymentCompleted
- WalletDebited
- WalletCredited