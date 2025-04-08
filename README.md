# 🛡️ Sham Beauty Lounge Platform (SBL Platform)

Full-stack management platform for beauty studios —  
includes customer management, appointment booking, payment handling, and an admin dashboard.

---

## 📦 Project Structure

```bash
sbl-platform/
├── backend/
│   ├── kunden-service/         # Customer Service (Spring Boot)
│   ├── kalender-service/       # Calendar Service (Spring Boot)
│   └── zahlung-service/        # Payment Service (Spring Boot)
├── frontend/
│   └── admin-dashboard/        # Admin UI (Next.js + TailwindCSS)
├── docker-compose.yml          # Docker setup for PostgreSQL, Kafka, Zookeeper
└── README.md                   # This file
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

| Task | Command |
|:-----|:--------|
| Start all services | `docker-compose up --build` |
| Start customer backend | `./mvnw spring-boot:run` inside `backend/kunden-service` |
| Start frontend | `npm run dev` inside `frontend/admin-dashboard` |

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

This project is licensed under the MIT License.
