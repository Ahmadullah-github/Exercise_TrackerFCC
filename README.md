# 🏋️ Exercise Tracker Microservice

## 📌 Project Description
The **Exercise Tracker Microservice** is a backend application that allows users to create accounts, log their exercises with details such as duration and date, and retrieve their workout logs. This project is built as part of the **freeCodeCamp Back End Development and APIs Certification**.

## 🚀 Features
- 📌 **User Management**: Create new users and retrieve user data.
- 🏃 **Exercise Logging**: Add exercises with a description, duration, and date.
- 📜 **User Logs**: Retrieve exercise history with optional filters (date range & limit).
- 🔗 **REST API**: Built using Express.js and MongoDB.
- 🌍 **CORS Enabled**: Allows cross-origin requests.

## 🛠️ Tech Stack
- **Node.js** 🟢
- **Express.js** ⚡
- **MongoDB + Mongoose** 🍃
- **dotenv** 🔐 (for environment variables)
- **CORS** 🌍

## 🔧 Setup and Installation
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/exercise-tracker.git
cd exercise-tracker
```
### 2️⃣ Install Dependencies
```bash
npm install
```
### 3️⃣ Setup Environment Variables
Create a `.env` file in the root directory and add your MongoDB connection string:
```env
DBURL=mongodb+srv://your_mongodb_connection_string
PORT=3000
```
### 4️⃣ Start the Server
```bash
npm start
```
The server will run at **http://localhost:3000** 🚀

## 📡 API Endpoints
### 🔹 Create a New User
**POST** `/api/users`
```json
{
  "username": "JohnDoe"
}
```
📥 **Response:**
```json
{
  "username": "JohnDoe",
  "_id": "64fddc2a8b5c3f0012345678"
}
```

### 🔹 Get All Users
**GET** `/api/users`

### 🔹 Add Exercise for a User
**POST** `/api/users/:_id/exercises`
```json
{
  "description": "Running",
  "duration": 30,
  "date": "2024-03-15"
}
```
📥 **Response:**
```json
{
  "_id": "64fddc2a8b5c3f0012345678",
  "username": "JohnDoe",
  "date": "Fri Mar 15 2024",
  "duration": 30,
  "description": "Running"
}
```

### 🔹 Get User Exercise Log
**GET** `/api/users/:_id/logs?from=YYYY-MM-DD&to=YYYY-MM-DD&limit=NUMBER`

📥 **Response:**
```json
{
  "_id": "64fddc2a8b5c3f0012345678",
  "username": "JohnDoe",
  "count": 2,
  "log": [
    {
      "description": "Running",
      "duration": 30,
      "date": "Fri Mar 15 2024"
    }
  ]
}
```

## 🛠️ Deployment
You can deploy this project on platforms like **Heroku, Vercel, or Render**.

## 🏆 Acknowledgments
This project is part of the **freeCodeCamp Back End Development and APIs Certification**.

---
🚀 **Happy Coding!** 🎉

