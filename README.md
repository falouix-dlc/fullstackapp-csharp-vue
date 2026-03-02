# 🚀 Full Stack App — .NET 10 + Vue + PostgreSQL + Docker

A modern full-stack application built with:

- ⚙️ ASP.NET Core (.NET 10)
- 🎨 Vue 3 + Vite
- 🐘 PostgreSQL
- 🐳 Docker & Docker Compose

---

## 🏗 Project Architecture

Frontend (Vue + Vite) → Backend (.NET API) → PostgreSQL
localhost:5173  →  localhost:5000  →  localhost:5432

📁 Project Structure

root/
│
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


🐳 Run in Development Mode
  1️⃣ Build and start everything : docker-compose -f docker-compose.dev.yml up --build
2️⃣ Access the app
  Frontend → http://localhost:5173
  Backend API → http://localhost:5000
  PostgreSQL → localhost:5432
Database Configuration
  Host: db
  Port: 5432
  Database: myappdb
  Username: postgres
  Password: postgres
Connection string used inside Docker:Host=db;Port=5432;Database=myappdb;Username=postgres;Password=postgres

🛠 Tech Stack
  Backend
    ASP.NET Core 10
    Entity Framework Core
    Npgsql (PostgreSQL provider)

  Frontend
    Vue 3
    Vite
    DevOps
    Docker
    Docker Compose
