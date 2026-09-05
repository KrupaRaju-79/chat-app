# Real-Time Chat Application

A full-stack **real-time chat application** built with **React, Node.js, Express.js, MongoDB, and Socket.io**. The application enables users to communicate in real time with secure authentication, private messaging, group conversations, and persistent chat history.

## ✨ Features

* 🔐 **JWT Authentication** – Secure user registration and login
* 💬 **Real-Time Messaging** – Instant message delivery using Socket.io
* 👤 **Private Messaging** – One-to-one conversations between users
* 👥 **Group Conversations** – Create and participate in group chats
* 💾 **Message Persistence** – Store and retrieve messages using MongoDB
* 🛡️ **Protected Routes** – Secure API endpoints with authentication middleware
* 🔄 **Real-Time Updates** – Messages are delivered without refreshing the page
* 👤 **Profile Management** – Manage user profile information
* 📱 **Responsive UI** – Modern interface that works across different screen sizes
* 📁 **File Upload Support** – Handle file sharing through the application

## 🛠️ Tech Stack

### Frontend

* **React 18**
* **Vite**
* **Redux Toolkit**
* **Tailwind CSS**
* **Socket.io Client**
* **Lucide React**

### Backend

* **Node.js**
* **Express.js**
* **Socket.io**
* **MongoDB**
* **Mongoose**
* **JWT**
* **Multer**

## 🏗️ Architecture

```text
┌─────────────────────┐
│     React Client    │
│  Vite + Redux       │
└──────────┬──────────┘
           │
           │ REST API
           │ WebSocket
           ▼
┌─────────────────────┐
│   Node.js Server    │
│ Express + Socket.io │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│       MongoDB       │
│  Users & Messages   │
└─────────────────────┘
```

## 📁 Project Structure

```text
chat-app/
│
├── client/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── package.json
│   └── ...
│
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites

Make sure the following are installed on your system:

* Node.js 18 or higher
* npm
* MongoDB or MongoDB Atlas

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/chat-app.git
cd chat-app
```

### 2. Install Backend Dependencies

```bash
cd server
npm install
```

### 3. Install Frontend Dependencies

```bash
cd ../client
npm install
```

## ⚙️ Environment Variables

### Server

Create a `.env` file inside the `server` directory:

```env
MONGODB_URI=your-mongodb-connection-string
JWT_SECRET=your-jwt-secret
PORT=8747
NODE_ENV=development
ORIGIN=http://localhost:5173
```

### Client

Create a `.env` file inside the `client` directory:

```env
VITE_SERVER_URL=http://localhost:8747
VITE_API_URL=http://localhost:8747/api
```

**Do not commit `.env` files or expose database credentials, API keys, or JWT secrets on GitHub.**

## ▶️ Running the Application

### Start the Backend

Open a terminal and run:

```bash
cd server
npm start
```

### Start the Frontend

Open another terminal:

```bash
cd client
npm run dev
```

The frontend will normally be available at:

```text
http://localhost:5173
```

## 🔑 Authentication

The application uses **JSON Web Tokens (JWT)** for authentication.

The authentication flow includes:

1. User registration/login
2. Server validates credentials
3. JWT token is generated
4. Token is used for authenticated requests
5. Protected routes verify the token using middleware

## ⚡ Real-Time Communication

**Socket.io** is used to establish real-time communication between clients and the server.

When a user sends a message:

```text
User A
   │
   │ Send Message
   ▼
Socket.io Server
   │
   │ Real-Time Event
   ▼
User B
```

This allows messages to appear instantly without requiring the user to refresh the page.

## 📌 Key Concepts Demonstrated

* Full-stack web application development
* REST API development
* JWT authentication
* WebSocket communication
* Socket.io event handling
* MongoDB database integration
* Mongoose data modeling
* Redux state management
* Protected API routes
* File upload handling
* Responsive frontend development

## 📄 License

This project is licensed under the MIT License.
