# 🚀 Full Stack App — .NET 10 + Vue + PostgreSQL + Docker

A modern full-stack application built with:

- ⚙️ ASP.NET Core (.NET 10)
- 🎨 Vue 3 + Vite
- 🐘 PostgreSQL
- 🐳 Docker & Docker Compose

## 📋 Table of Contents

- [Project Architecture](#project-architecture)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Tech Stack](#tech-stack)

---

## 🏗️ Project Architecture

```
Frontend (Vue + Vite) → Backend (.NET API) → PostgreSQL
localhost:5173  →  localhost:5000  →  localhost:5432
```

## 📁 Project Structure

```
root/
├── backend/
│   ├── api/
│   ├── Dockerfile
│   └── Dockerfile.dev
│
├── frontend/
│   ├── src/
│   ├── Dockerfile
│   └── Dockerfile.dev
│
├── docker-compose.dev.yml
└── docker-compose.yml
```

## 🚀 Getting Started

### Prerequisites

- Docker & Docker Compose installed
- Git

### Run in Development Mode

1. **Build and start everything:**
   ```bash
   docker-compose -f docker-compose.dev.yml up --build
   ```

2. **Access the application:**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:5000
   - PostgreSQL: localhost:5432

### Database Configuration

| Property | Value |
|----------|-------|
| Host | db |
| Port | 5432 |
| Database | myappdb |
| Username | postgres |
| Password | postgres |

**Connection String (Docker):**
```
Host=db;Port=5432;Database=myappdb;Username=postgres;Password=postgres
```

## 🛠️ Tech Stack

### Backend
- ASP.NET Core 10
- Entity Framework Core
- Npgsql (PostgreSQL provider)

### Frontend
- Vue 3
- Vite

### DevOps
- Docker
- Docker Compose

---

## 📝 License

This project is open source and available under the MIT License.