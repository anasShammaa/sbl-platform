# 🛠️ Backend Services

## Structure
- `kunden-service/` — Customer management microservice
- `kalender-service/` — Calendar and scheduling microservice
- `zahlung-service/` — Payment microservice
- `parent-pom/` — Centralized dependency and plugin management
- `api-collection/` — OpenAPI generated interfaces (internal + external)

## How to run locally
```bash
cd backend/your-service
./mvnw spring-boot:run
```

Or with Docker Compose:
```bash
docker-compose up
```
