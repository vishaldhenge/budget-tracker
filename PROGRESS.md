# 📊 BudgetTracker Project Progress

## 📂 Project Structure
BudgetTracker/
│── BudgetTracker.Api/ # API Layer
│
│── BudgetTracker.Dal/ # Data Access Layer
│
│── BudgetTracker.Database/ # Database scripts
│ │── SchemaChanges/ # schema migrations (tables, constraints, etc.)
│ │ ├── SchemaChanges.sql
│
│ │── DataChanges/ # data scripts (seeding, inserts, reference data)
│ │ ├── DataChanges.sql
│
│── budget-tracker-frontend/ # Angular frontend
│ │── projects/
│ │ │── app-main/ # main budgeting app (after login)
│ │ │── app-access/ # authentication / login app

---

## 🚀 Progress by Day

### **Day 1 – Project Setup**
- Created GitHub repo  
- Added `.gitignore` (VS template)  
- Added `README.md` (description, roadmap, license)  
- Decided repo structure (`BudgetTracker.Api`, `BudgetTracker.Dal`, `budget-tracker-frontend`)  
- Angular multi-app setup (`app-access`, `app-main`)  
- **Tech choices:**  
  - Backend: ASP.NET Core 8 Web API  
  - Database: PostgreSQL + Dapper  
  - Frontend: Angular 16+ with SCSS  
  - Deployment: Angular served by ASP.NET static files  

---

### **Day 2 – Database Design**
- Designed schema: `users`, `user_profiles`, `roles`, `user_roles`  
- **Conventions:**  
  - `id BIGSERIAL PRIMARY KEY`  
  - Audit fields (`created_by`, `created_date`, etc.)  
  - Foreign keys with clear naming (`fk_user_profiles_users`)  
- Decided to use **BCrypt** for password hashing  
- Inserted initial **Admin record** via script (`DataChanges.sql`)  
- Added `BudgetTracker.Database/SchemaChanges` & `DataChanges` folders  
- Created `SchemaChanges.sql` & `DataChanges.sql`  

---

### **Day 3 (Planned) – Auth + Integration**
- Configure Angular build output into `.NET wwwroot`  
- Add build scripts with `concurrently`  
- Implement `/api/auth/login` (JWT + role claims)  
- Configure ASP.NET Core JWT auth (`AddAuthentication().AddJwtBearer`)  
- Add `[Authorize]` and `[Authorize(Roles="...")]` to sample endpoints  
- Angular `app-access`: login form → call API → store token → redirect to `app-main`  
- Angular `app-main`: check token → fetch profile from protected API  
- Add Angular `HttpInterceptor` to attach JWT + handle 401 errors  
- (Optional) Role-based route guards in Angular  

---
