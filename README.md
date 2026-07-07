# MERNexus

## What This Is

**MERNexus** is a full-stack admin dashboard application built with the **MERN** stack (**MongoDB, Express, React, Node.js**). It provides a complete **CRUD** interface for managing **Users, Products, and Orders** through a modern dark-themed React frontend and a REST API backend powered by Express and MongoDB.

---

## Tech Stack

### Languages

- JavaScript (98.5%)
- CSS
- HTML

### Frameworks & Runtime

- Node.js
- Express 5.2
- React 19
- Vite

### Libraries

- Mongoose (MongoDB data modeling)
- Tailwind CSS (Styling)
- React Router (Routing)
- Fetch API (HTTP Requests)

---

## Project Structure

```text
MERN-project/
│
├── backend/
│   ├── src/
│   │   ├── config/          # MongoDB connection setup
│   │   ├── controllers/     # Request handlers
│   │   │   ├── users
│   │   │   ├── products
│   │   │   └── orders
│   │   ├── model/           # Mongoose schemas
│   │   ├── routes/          # REST API routes
│   │   └── app.js           # Express app configuration
│   │
│   ├── server.js            # Backend entry point
│   └── package.json
│
└── frontend/
    ├── src/
    │   ├── components/      # Reusable UI components
    │   │   ├── Navbar
    │   │   ├── AlertMessage
    │   │   ├── ConfirmModal
    │   │   └── ...
    │   │
    │   ├── pages/           # Dashboard pages
    │   │   ├── Home
    │   │   ├── Users
    │   │   ├── Products
    │   │   └── Orders
    │   │
    │   ├── services/        # API wrappers
    │   └── App.jsx          # Main routing
    │
    ├── public/
    ├── vite.config.js
    └── package.json
```

---

## Architecture

```text
React Components
        │
        ▼
Service Layer (Fetch API)
        │
        ▼
Express Routes
        │
        ▼
Controllers
        │
        ▼
Mongoose Models
        │
        ▼
MongoDB
```

The frontend runs as a **single-page application** on **port 5173**, communicating with the backend through REST API calls.

The backend exposes the following endpoints:

- `/users`
- `/products`
- `/orders`

Each endpoint is backed by a dedicated **Mongoose model**, with populated references used for order relationships.

---

# Getting Started

## 1. Clone the Repository

```bash
git clone <repository-url>
cd MERN-project
```

---

## 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file inside the **backend** directory:

```env
PORT=4000
MONGODB_URL=your_mongodb_atlas_connection_string
```

Start the backend server:

```bash
npm run dev
```

The backend will run at:

```text
http://localhost:4000
```

---

## 3. Frontend Setup

Open a new terminal:

```bash
cd frontend
npm install
```

(Optional) Create a `.env` file inside **frontend**:

```env
VITE_API_BASE_URL=http://localhost:4000
```

Start the frontend:

```bash
npm run dev
```

The frontend will run at:

```text
http://localhost:5173
```

---

## API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/users` | Get all users |
| POST | `/users` | Create a user |
| PUT | `/users/:id` | Update a user |
| DELETE | `/users/:id` | Delete a user |
| GET | `/products` | Get all products |
| POST | `/products` | Create a product |
| PUT | `/products/:id` | Update a product |
| DELETE | `/products/:id` | Delete a product |
| GET | `/orders` | Get all orders |
| POST | `/orders` | Create an order |
| PUT | `/orders/:id` | Update an order |
| DELETE | `/orders/:id` | Delete an order |

---

## Features

- Full CRUD operations
- RESTful API architecture
- React 19 + Vite frontend
- Express.js backend
- MongoDB with Mongoose
- Tailwind CSS UI
- React Router navigation
- Modular project structure
- Dark-themed admin dashboard
- API service layer abstraction
- Order relationships using Mongoose population

---

## Default Ports

| Service | Port |
|---------|------|
| Backend | **4000** |
| Frontend | **5173** |

---

## Data Flow

```text
React UI
   │
   ▼
API Services
   │
   ▼
Express Routes
   │
   ▼
Controllers
   │
   ▼
Mongoose Models
   │
   ▼
MongoDB
```
````
