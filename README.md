
# Task Management System API

A RESTful Task Management API built with **Node.js**, **TypeScript**, **PostgreSQL (TypeORM)**, and **JWT Authentication**.

---

## Tech Stack

- **Node.js** with **TypeScript**
- **Express.js**
- **TypeORM** with PostgreSQL
- **JWT** Authentication
- **JOI** for input validation
- **dotenv** for environment configuration

---

## Features

- ✅ User Registration & Login (JWT Auth)
- ✅ Get Authenticated User Profile
- ✅ Create, Read, Update, Delete Tasks
- ✅ Filter Tasks by Status
- ✅ Mark Task as Complete
- ✅ Proper error handling & validation
- ✅ Modular folder structure with clean code

---

## Authentication Flow

- On login, user receives a JWT token.
- Token must be sent in `Authorization` header (`Bearer <token>`) for protected routes.
- Middleware extracts user and attaches it to the request object.

---

##  API Endpoints

### Authentication

| Method | Endpoint         | Description           |
|--------|------------------|-----------------------|
| POST   | /api/auth/signup | Register new user     |
| POST   | /api/auth/login  | Login and get JWT     |

### User

| Method | Endpoint       | Description             |
|--------|----------------|-------------------------|
| GET    | /api/users/me  | Get user profile (auth) |

### Tasks

| Method | Endpoint                         | Description                   |
|--------|----------------------------------|-------------------------------|
| POST   | /api/tasks                       | Create new task (auth)        |
| GET    | /api/tasks                       | Get all tasks (auth)          |
| GET    | /api/tasks/:id                   | Get single task by ID         |
| PUT    | /api/tasks/:id                   | Update task                   |
| PATCH  | /api/tasks/:id/complete          | Mark task as completed        |
| DELETE | /api/tasks/:id                   | Delete task                   |

---

## Setup Instructions

```bash
# 1. Clone the repository
git clone https://github.com/Swathimuthukumarg/TaskManagementSystem.git
cd nodeProject

# 2. Install dependencies
npm install

# 3. Configure environment variables
cp .env.example .env
# Then edit .env to match your DB and JWT config

# 4. Run migrations (if applicable)
# TypeORM auto-sync is enabled, or use CLI

# 5. Start development server
npm run dev
```

---

## Folder Structure

```
src/
├── config/
├── controllers/
├── entities/
├── middlewares/
├── routes/
├── types/
├── utils/
├── index.ts
```

---

## Assumptions & Limitations

- Only basic user roles assumed; no admin logic.
- Token expires in 1 hour, refresh tokens not implemented.
- Basic error and validation included; extendable.

---

## API Documentation

- Postman Collection `docs/` folder.

---

## Author

- **Swathi Muthukumar**  
  Full Stack Developer | Node.js | React | PostgreSQL/MySQL | AWS 
  GitHub: [https://github.com/Swathimuthukumarg/nodeProject](https://github.com/Swathimuthukumarg/nodeProject)  
  LinkedIn: [https://linkedin.com/in/swathimuthukumarg](https://linkedin.com/in/swathimuthukumarg)  
  Email: swathimuthukumarg@gmail.com

---

## API Flow Diagram

Refer `docs/flow-diagram.png` for login → create task flow.
