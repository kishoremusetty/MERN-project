
What this is

MERNexus is a full-stack admin dashboard application built with the MERN stack (MongoDB, Express, React, Node). It provides a complete CRUD interface for managing users, products, and orders with a modern dark-themed React frontend and a REST API backend running on Express and MongoDB.

Stack
Language(s): JavaScript (98.5%), CSS, HTML
Framework / runtime: Node.js + Express 5.2 (backend), React 19 + Vite (frontend)

Notable libraries: Mongoose (data modeling), Tailwind CSS (styling), React Router (navigation), Fetch API (HTTP calls)


How it's organized
Code
MERN-project/
├── backend/                Express + MongoDB REST API
│   ├── src/
│   │   ├── config/        MongoDB connection setup
│   │   ├── controllers/    Request handlers (users, products, orders)
│   │   ├── model/         Mongoose schemas
│   │   ├── routes/        API endpoint definitions
│   │   └── app.js         Express app configuration
│   ├── server.js          Entry point
│   └── package.json       Dependencies
│
└── frontend/              React + Vite single-page app
    ├── src/
    │   ├── components/    Reusable UI (Navbar, AlertMessage, ConfirmModal, etc.)
    │   ├── pages/        Dashboard sections (Home, Users, Products, Orders)
    │   ├── services/     API wrappers for backend calls
    │   └── App.jsx       Main routing
    ├── public/           Static files
    ├── vite.config.js    Build configuration
    └── package.json      Dependencies

How it fits together: The frontend boots a single-page dashboard (React + Tailwind) on port 5173 that fetches data from the backend via REST calls to http://localhost:4000. The backend exposes /users, /products, and /orders endpoints, each backed by Mongoose models connected to MongoDB. Requests flow from React components → services layer (API wrappers) → Express controllers → Mongoose models → MongoDB, with populated references for order relationships.



How to run it
Backend setup:

bash
cd backend
npm install
# Create a .env file with:
# PORT=4000
# MONGODB_URL=your_mongodb_atlas_connection_string
npm run dev
Frontend setup (in a new terminal):

bash
cd frontend
npm install
# Optionally create a .env file with:
# VITE_API_BASE_URL=http://localhost:4000
npm run dev
The backend server listens on port 4000; the frontend Vite dev server starts on port 5173 (or the next available port).
