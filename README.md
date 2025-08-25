
```markdown
# LeadManager 

![LeadManager](https://img.shields.io/badge/Status-Active-brightgreen)
![Node.js](https://img.shields.io/badge/Backend-Node.js-blue)
![React](https://img.shields.io/badge/Frontend-React-61DAFB)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248)

LeadManager is a professional lead management portal with a modern React frontend and a Node.js/Express backend. It provides secure authentication, full CRUD for leads, real-time dashboards, and advanced filtering with AG Grid.

This repository contains both frontend and backend, enabling a full-stack development experience.

---

## 🔥 Features

### Frontend
- React 19 with hooks and functional components  
- AG Grid: sorting, filtering, server-side pagination  
- JWT-based authentication (login/register)  
- Responsive dashboard with real-time statistics and quick action cards  
- Forms with validation for lead creation/edit  
- Toast notifications for user feedback  
- Mobile-friendly design  

### Backend
- Node.js + Express API server  
- MongoDB with Mongoose models  
- JWT authentication + bcrypt password hashing  
- RESTful APIs for users and leads  
- Server-side pagination & filtering  
- Protected routes and middleware for security  

---

##  Tech Stack

| Frontend | Backend |
|----------|---------|
| React 19 | Node.js + Express |
| AG Grid | MongoDB + Mongoose |
| Tailwind CSS | JWT Authentication |
| React Router | bcrypt |
| Axios | CORS, dotenv |
| React Toastify | Nodemon (dev) |
| Vite | ESLint, Prettier |

---

## 📂 Project Structure

### Frontend (`client/`)
```

src/
├── api/            # Axios API config
├── components/     # Layout, Navbar, ProtectedRoute
├── context/        # AuthContext
├── pages/          # Login, Register, LeadsList, LeadForm, Dashboard
├── App.jsx         # Main app
├── main.jsx        # Entry point
└── index.css       # Global styles

```

### Backend (`server/`)
```

server/
├── config/         # DB connection
├── middleware/     # Auth & error handling
├── models/         # User and Lead schemas
├── routes/         # Auth and Lead routes
├── controllers/    # API logic
├── utils/          # Scripts & helpers
├── server.js       # Entry point
└── .env            # Environment variables

````

---

##  UML Diagrams

### 1️Class Diagram (Backend Models)

```mermaid
classDiagram
    class User {
        +String name
        +String email
        +String password
        +String role
        +timestamps
        +verifyPassword()
    }
    class Lead {
        +String first_name
        +String last_name
        +String email
        +String phone
        +String company
        +String city
        +String state
        +String source
        +String status
        +Number score
        +Number lead_value
        +Boolean is_qualified
        +timestamps
    }
    User "1" -- "many" Lead : manages
````

### API Flow Diagram

```mermaid
graph TD
    A[Frontend React App] -->|Axios Requests| B[Backend Express API]
    B --> C[MongoDB Database]
    B -->|JWT Authentication| B
    C --> B
    B --> A
```

---

##  Setup & Run

### Prerequisites

* Node.js v16+
* MongoDB (local or Atlas)
* npm or yarn

### Backend

```bash
cd server
npm install
# create .env
# PORT=5000
# MONGO_URI=<your_mongo_uri>
# JWT_SECRET=<your_secret>
npm run dev
```

### Frontend

```bash
cd client
npm install
# create .env
# VITE_API_URL=http://localhost:5000/api
# VITE_APP_NAME=LeadManager
# VITE_APP_VERSION=1.0.0
npm run dev
```

> Frontend: `http://localhost:5173`
> Backend: `http://localhost:5000`

---

##  Key API Endpoints

### Auth

* `POST /api/auth/register` → Register
* `POST /api/auth/login` → Login
* `POST /api/auth/logout` → Logout
* `GET /api/auth/me` → Current user

### Leads

* `GET /api/leads` → Fetch leads (with filters/pagination)
* `POST /api/leads` → Create lead
* `PUT /api/leads/:id` → Update lead
* `DELETE /api/leads/:id` → Delete lead
* `GET /api/leads/:id` → Single lead

---

## Development Scripts

### Frontend

* `npm run dev` → Start dev server
* `npm run build` → Build production
* `npm run preview` → Preview production build

### Backend

* `npm run dev` → Start server with nodemon
* `npm start` → Production start
* `npm run lint` → Run ESLint

---

##  Commit Guidelines

* `chore:` initial setup
* `feat(auth):` add authentication
* `feat(leads):` CRUD APIs
* `feat(ui):` AG Grid integration
* `fix:` validation & bugs
* `docs:` update README
* `refactor:` structure & reusable code
* `final:` cleanup & production readiness

---

##  Contributing

* Follow existing code style
* Add proper error handling & loading states
* Test on different screen sizes
* Update documentation as needed

---

## License

This project is part of the **LeadManager assignment** for educational purposes.

```

