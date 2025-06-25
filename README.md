# DPDzero

It is a multi-service application using Docker, built with:

- ⚙️ Go (service1)
- 🐍 Python (service2)
- 🌐 NGINX (as a reverse proxy)

---

## 🔧 Technologies Used

- **Golang (1.23.2)** – API server with two endpoints
- **Python (3.10)** – Secondary API server
- **NGINX** – Reverse proxy between services
- **Docker & Docker Compose** – For containerized development

---

## 📂 Project Structure

Devops_Internship_Assignment/
├── service1/ # Go service
│ ├── main.go
│ ├── go.mod
│ └── Dockerfile
├── service2/ # Python service
│ ├── app.py
│ └── Dockerfile
├── nginx/
│ └── default.conf # NGINX config
├── docker-compose.yml
└── .gitignore

---

## 🚀 API Endpoints

### 🔹 Service 1 (Go) – `http://localhost:8080`

| Method | Endpoint     | Description             |
|--------|--------------|-------------------------|
| GET    | `/ping`      | Returns service, status |
| GET    | `/hello`     | Returns Hello from service1|

---

### 🔹 Service 2 (Python) – `http://localhost:8080`

| Method | Endpoint     | Description                 |
|--------|--------------|-----------------------------|
| GET    | `/greet`     | Returns service, status    |
| GET    | `/status`    | Returns Hello from service2 |

---

## 🧪 Getting Started

### Prerequisites

- Docker Desktop
- Git

### Run Locally

```bash
docker-compose up --build
Access Endpoints
Go Service (via NGINX):

http://localhost:8080/service1/ping

http://localhost:8080/service1/hello

Python Service (via NGINX):

http://localhost:8080/service2/ping

http://localhost:8080/service2/hello
