# add-search-user


A full-stack web application for managing users with features to **add, search, and list users**.  
This project is built with **Spring Boot (backend)** and **React.js (frontend)**, using **PostgreSQL** as the database.

## 🚀 Features
- **Add User**: Create new user accounts with validation and secure password encryption.
- **Search Users**: Find users by username, first name, last name, email, or user ID.
- **List Users**: View all registered users in a comprehensive table format.
- **Authentication**: Supports JWT-based authentication (or Basic Auth fallback).
- **Validation**: Both client-side (React) and server-side (Spring Boot).

## 🛠️ Tech Stack
- **Backend**: Spring Boot (Java), PostgreSQL, JWT authentication
- **Frontend**: React.js, Axios, TailwindCSS
- **Database**: PostgreSQL

## 📂 Project Structure
```
user-management-fullstack/
│── backend/        # Spring Boot backend with APIs for Add/Search/List users
│── frontend/       # React frontend with UI for user management
│── README.md       # Project documentation
```

## ⚙️ Setup Instructions

### 1. Backend (Spring Boot)
1. Navigate to backend folder:
   ```bash
   cd backend
   mvn spring-boot:run
   ```
2. The backend will run on `http://localhost:8080`.

### 2. Frontend (React)
1. Navigate to frontend folder:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```
2. The frontend will run on `http://localhost:5173`.

## 🧪 API Endpoints

### Add User API
- **POST** `/api/users`
- Request Body:
```json
{
  "username": "Bhavana",
  "firstName": "H B",
  "lastName": "Bhavana",
  "email": "bhavanahb95@gmail.com",
  "password": "Bhavana@9686"
}
```
- Response:
```json
{
  "status": "success",
  "userId": 1
}
```

### Search User API
- **POST** `/api/users/search`
- Request Body:
```json
{
  "username": "Bhavana"
}
```
- Response:
```json
[
  {
    "id": 1,
    "username": "Bhavana",
    "firstName": "H B",
    "lastName": "Bhavana",
    "email": "bhavanahb95@gmail.com"
  }
]
```

## 📌 Notes
- Ensure PostgreSQL is running and configured in `application.properties`.
- Default port: `5432`
- Update DB credentials before running.

---
