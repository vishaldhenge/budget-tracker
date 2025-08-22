# 💰 Budget Tracker App

A simple web application to track **income, expenses, and savings** — designed for the Indian audience with future UPI support.

## 🛠️ Tech Stack
- **Frontend:** Angular 16+
- **Backend:** ASP.NET Core 8 (Web API)
- **Database:** PostgreSQL
- **ORM:** Dapper

## ✨ Features (Planned & In-Progress)
- [ ] User authentication (JWT-based)
- [ ] Add / edit / delete transactions
- [ ] Categorize expenses (Food, Travel, Bills, etc.)
- [ ] Dashboard with charts & summaries
- [ ] UPI/Bank integration (future)
- [ ] Export to Excel/PDF

## 🚀 Getting Started

### 1) Clone the repo
```bash
git clone https://github.com/your-username/budget-tracker.git
cd budget-tracker
```

### 2) Backend Setup (ASP.NET Core)
```bash
cd backend
dotnet restore
dotnet run
```

### 3) Frontend Setup (Angular)
```bash
cd frontend
npm install
ng serve -o
```

### 4) Database (PostgreSQL)
- Install PostgreSQL & pgAdmin  
- Create a database named `budget_tracker`  
- Add the connection string in `appsettings.json`

## 🗺️ Roadmap (Working Order)
1. ✅ Repo & Project Setup  
2. 🔄 API boilerplate with PostgreSQL + Dapper  
3. 🔄 Basic Angular UI (Login, Dashboard Shell)  
4. ⏳ Authentication & Authorization (JWT)  
5. ⏳ Transaction APIs (CRUD)  
6. ⏳ Dashboard with charts  
7. ⏳ Polish UI + UPI integration

## 📜 License
This project is licensed under the **MIT License**.
