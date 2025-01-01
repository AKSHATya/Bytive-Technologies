# 📚 **Task Management API**

This is a **Task Management API** built with **Node.js**, **Express.js**, **PostgreSQL**, and **JWT Authentication**. It provides endpoints to manage tasks, including creating, reading, updating, and deleting tasks securely.

---

## 🚀 **Features**
- User **Signup** and **Login** with JWT Authentication.
- Secure **CRUD operations** for tasks.
- Modular folder structure.
- Environment variables for sensitive data.

---

## 🛠️ **Technologies Used**
- **Node.js**
- **Express.js**
- **PostgreSQL**
- **JWT (JSON Web Tokens)**
- **Bcrypt** (Password Hashing)
- **dotenv** (Environment Variables)

---

## 📂 **Folder Structure**
```
/server
├── /controllers     # Business logic for tasks and authentication
├── /db             # Database connection configuration
├── /middleware     # JWT authentication middleware
├── /routes         # API route definitions
├── index.js        # Server entry point
└── .env           # Environment variables
```

---

## 📦 **Requirements**
Ensure you have the following installed on your system:

```bash
- Node.js (v14+ recommended)
- PostgreSQL
- npm (Node Package Manager)
```

---

## ⚙️ **Setup Instructions**

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/AKSHATya/Bytive-Technologies.git
```
### 2️⃣ **Extract the Zip File**
Downloaded the repository as a .zip file and follow these steps:

1.Extract the zip file in your preferred location.
2.Navigate to the server folder.

### 3️⃣ **Install Dependencies**
```bash
npm install
```


### 4️⃣ **Setup Database**
Run the following commands in your PostgreSQL shell to create the database and tables:
```sql
CREATE DATABASE backend;

CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE tasks (
    id SERIAL PRIMARY KEY,
    title VARCHAR(100) NOT NULL,
    description TEXT,
    status VARCHAR(20) DEFAULT 'pending'
);
```

### 5️⃣ **Start the Server**
```bash
node index.js 
```

The server will start at: **http://localhost:3000**

---

## 📡 **API Endpoints**

### **Authentication Routes:**
- **POST /api/signup** → Register a new user.
- **POST /api/login** → Authenticate and receive a JWT token.

### **Task Routes (Protected by JWT):**
- **POST /api/tasks** → Create a new task.
- **GET /api/tasks** → Get all tasks.
- **GET /api/tasks/:id** → Get a task by ID.
- **PUT /api/tasks/:id** → Update a task.
- **DELETE /api/tasks/:id** → Delete a task.

---

## 🔑 **Authorization**
Include the JWT token in the **Authorization Header** for protected routes:
```http
Authorization: Bearer <your_token>
```

---

## 🧪 **Testing the API**
You can test the API using tools like:
- **Postman**
- **cURL**

Example cURL request:
```bash
curl -X GET http://localhost:3000/api/tasks \
-H "Authorization: Bearer <your_token>"
```

---

Happy Coding! 🚀✨

**Author:** Akshat  
**GitHub:**   https://github.com/AKSHATya
**Email:** akshaty961@gmail.com
