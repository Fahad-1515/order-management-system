# Cloud-Native Order Management System (Microservices)

A **production-ready cloud-native backend system** built using **Spring Boot microservices**, **MongoDB Atlas**, **Docker**, and **JWT authentication**, designed for **free-tier cloud deployment on Render**.

---

## Architecture Overview

- Monorepo Microservices Architecture
- API Gateway Pattern
- Stateless JWT Authentication
- Independent service deployment

Client
|
API Gateway
|

| | |
User Service Order Service Inventory Service
|
MongoDB Atlas (Free Tier)

---

## 🛠 Tech Stack

| Layer      | Technology                |
| ---------- | ------------------------- |
| Backend    | Java 17, Spring Boot 3    |
| Database   | MongoDB Atlas (Free Tier) |
| Security   | JWT Authentication        |
| Containers | Docker                    |
| CI/CD      | GitHub Actions            |
| Deployment | Render                    |

---

## 📦 Microservices

### 👤 User Service

- User registration and login
- JWT token generation
- Secure authentication
- MongoDB persistence

### 📦 Order Service

- Create and fetch orders
- Communicates with Inventory Service
- MongoDB order storage

### 📊 Inventory Service

- Product and stock management
- Stock validation on order placement
- MongoDB inventory storage

### 🌐 API Gateway

- Single entry point for all requests
- JWT validation
- Routes requests to backend services.

## 🐳 Docker (Local Development)

> `docker-compose` is used **only for local development**.  
> Render deploys each microservice independently.

```bash
docker-compose up --build

#Environment Variables
PORT=8080
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/db
JWT_SECRET=super-secret-key.

```
