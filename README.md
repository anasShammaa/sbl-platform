# 🛡️ Sham Beauty Lounge Platform (SBL Platform)

Full-stack management platform for beauty studios —  
includes customer management, appointment booking, payment handling, and an admin dashboard.

---

## 📦 Project Structure

```bash
sbl-platform/
├── backend/                  # All backend services
│   ├── kunden-service/        # Customer management service
│   ├── kalender-service/      # Calendar scheduling service
│   ├── zahlung-service/       # Payment service
│   ├── parent-pom/            # Centralized dependency management (Spring Boot versions, etc.)
│   ├── api-collection/        # OpenAPI collection for external/internal APIs
│   └── README.md              # Backend instructions
├── frontend/                  # Frontend apps
│   ├── admin-dashboard/       # Admin dashboard app
│   └── README.md              # Frontend instructions
├── k8s/                       # Kubernetes manifests (future)
├── .github/                   # GitHub workflows and PR templates
├── docker-compose.yml         # Docker orchestration for local development
├── README.md                  # Main project documentation
└── LICENSE                    # Project license

```

---

## 🚀 Technologies Used

- **Backend:** Java 21, Spring Boot 3
- **Frontend:** React (Next.js 14), TailwindCSS, Shadcn UI
- **Messaging:** Apache Kafka
- **Database:** PostgreSQL 15
- **Monitoring:** Grafana, Prometheus, Loki (planned)
- **DevOps:** Docker Compose
- **Authentication:** Auth0 (planned)

---

## 🖥️ Local Development Setup

### 1. Clone the repository

```bash
git clone git@github.com:anasShammaa/sbl-platform.git
cd sbl-platform
```

### 2. Start Docker services

```bash
docker-compose up --build
```

This will start:

- PostgreSQL at `localhost:5432`
- Kafka at `localhost:9092`
- Zookeeper at `localhost:2181`

### 3. Start Backend Services

Start each microservice individually.

Example to start the Customer Service:

```bash
cd backend/kunden-service
./mvnw spring-boot:run
```

Repeat for other services (`kalender-service`, `zahlung-service`).

### 4. Start Frontend Admin Dashboard

```bash
cd frontend/admin-dashboard
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🛠️ Project Commands

| Task                   | Command                                                  |
|:-----------------------|:---------------------------------------------------------|
| Start all services     | `docker-compose up --build`                              |
| Start customer backend | `./mvnw spring-boot:run` inside `backend/kunden-service` |
| Start frontend         | `npm run dev` inside `frontend/admin-dashboard`          |

---

## 📈 Future Plans

- Online booking system for customers
- Payment integration with SumUp
- Staff management
- Public website for customers
- Monitoring dashboards (Grafana + Prometheus)
- AWS hosting and full CI/CD pipelines
- Real-time event-driven architecture with Kafka

---

## 📜 License

This project is licensed under the MIT Licence.

---

## 🧩 Git Workflow

- Branch: `develop` → `feature/*`, `bugfix/*`
- PRs must be created to `develop`
- Direct commits to `master` and `develop` are **forbidden**

---

## 📊 Badges

[![Docker Hub](https://img.shields.io/badge/DockerHub-SBL--Platform-blue)](https://hub.docker.com/)
[![Code Coverage](https://img.shields.io/badge/coverage-90%25-brightgreen)](https://your-codecov-link)
[![Sonar Quality Gate](https://sonarcloud.io/api/project_badges/measure?project=anasShammaa_sbl-platform&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=anasShammaa_sbl-platform)

---