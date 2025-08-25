LeadManager

LeadManager is a professional lead management portal with a modern React frontend and a Node.js/Express backend. It provides secure user authentication, full CRUD for leads, real-time dashboards, and advanced filtering using AG Grid.

This repository contains both the frontend and backend, enabling easy local setup and full-stack development experience.

----Features-----
Frontend

React 19 with hooks and functional components

AG Grid for data display, sorting, filtering, and server-side pagination

JWT-based authentication (login/register)

Responsive dashboard with quick action cards and real-time statistics

Forms with validation for lead creation/edit

Toast notifications for user feedback

Mobile-friendly design

Backend

Node.js + Express API server

MongoDB with Mongoose models

User authentication with JWT and bcrypt password hashing

RESTful APIs for leads and user management

Server-side pagination, filtering, and status tracking

Protected routes and middleware for security

 Tech Stack
Frontend	Backend
React 19	Node.js + Express
AG Grid	MongoDB + Mongoose
Tailwind CSS	JWT Authentication
React Router	bcrypt
Axios	CORS, dotenv
React Toastify	Nodemon (dev)
Vite	ESLint, Prettier
📂 Project Structure
Frontend (client/)
src/
├── api/            # Axios API config
├── components/     # Layout, Navbar, ProtectedRoute
├── context/        # AuthContext
├── pages/          # Login, Register, LeadsList, LeadForm, Dashboard
├── App.jsx         # Main app
├── main.jsx        # Entry point
└── index.css       # Global styles

Backend (server/)
server/
├── config/         # DB connection
├── middleware/     # Auth and error handling
├── models/         # User and Lead schemas
├── routes/         # Auth and Lead routes
├── controllers/    # Logic for APIs
├── utils/          # Scripts, helpers
├── server.js       # Entry point
└── .env            # Environment variables

⚡ Setup & Run
Prerequisites

Node.js v16+

MongoDB (local or Atlas)

npm or yarn

Backend Setup
cd server
npm install
# create .env with:
# PORT=5000
# MONGO_URI=<your_mongo_uri>
# JWT_SECRET=<your_secret>
npm run dev

Frontend Setup
cd client
npm install
# create .env with:
# VITE_API_URL=http://localhost:5000/api
# VITE_APP_NAME=LeadManager
# VITE_APP_VERSION=1.0.0
npm run dev


The frontend runs on http://localhost:5173 and connects to the backend at http://localhost:5000.

🔑 Key API Endpoints
Auth

POST /api/auth/register → Register

POST /api/auth/login → Login

POST /api/auth/logout → Logout

GET /api/auth/me → Current user

Leads

GET /api/leads → Fetch leads (with filters/pagination)

POST /api/leads → Create lead

PUT /api/leads/:id → Update lead

DELETE /api/leads/:id → Delete lead

GET /api/leads/:id → Single lead

🏗 Development Scripts
Frontend

npm run dev → Start dev server

npm run build → Build production

npm run preview → Preview production build

Backend

npm run dev → Start dev server with nodemon

npm start → Production start

npm run lint → Run ESLint

 Commit Guidelines

chore: initial project setup (client + server)

feat(auth): add JWT authentication

feat(leads): implement CRUD APIs

feat(ui): integrate AG Grid

fix: validation and bug fixes

docs: update README

refactor: improve structure & reusable code

final: cleanup and production readiness

License

This project is part of the LeadManager assignment for educational and assessment purposes.
