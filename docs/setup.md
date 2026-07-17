# Development Setup

## Prerequisites

- Java 21+
- Maven 3.9+
- PostgreSQL 16+
- Redis
- Apache Kafka
- Docker Desktop
- Kubernetes (Minikube or Docker Desktop)
- Git
- IntelliJ IDEA

---

## Clone Repository

```bash
git clone https://github.com/<username>/AIShield-Pay.git
```

---

## Run Infrastructure

```bash
docker compose up -d
```

---

## Services

| Service | Port |
|----------|------|
| Gateway | 8080 |
| Auth | 8081 |
| Payment | 8082 |
| User | 8083 |
| Kafka | 9092 |
| PostgreSQL | 5432 |
| Redis | 6379 |

---

## Build

```bash
mvn clean install
```

---

## Run

```bash
mvn spring-boot:run
```

---

## API Documentation

```
http://localhost:8080/swagger-ui/index.html
```

---

## Future

- CI/CD
- Kubernetes
- Helm Charts
- Monitoring
- AI Agent Integration