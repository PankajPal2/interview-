# 🤖 Real-Time AI Interview Platform

A high-performance, full-stack application designed to help candidates prepare for interviews using AI. The platform allows users to manage their resumes, receive AI-generated questions based on their experience, and simulate real-time interview scenarios.

---

## 🌟 Key Features

### 1. **Premium Landing Page** (Frontend)
- **Sleek Design**: Modern dark theme with glassmorphism and indigo/pink gradients.
- **Micro-Animations**: Smooth scroll reveal and hover effects for a premium feel.
- **Vite-Powered**: Fast development and optimized builds.
- **Modern CSS**: Custom design system with tokens in `src/index.css`.

### 2. **Secure Authentication** (Full Stack)
- **JWT-Based**: Industry-standard JSON Web Token security.
- **Real-time Validation**: Instant feedback on form inputs (email format, password strength).
- **Protected Routes**: Secure dashboard access ensures only logged-in users can participate.

### 3. **Smart Resume Management** (Full Stack)
- **Drag-and-Drop**: Easy file upload interface in the React dashboard.
- **Validation**: Support for `.pdf`, `.doc`, and `.docx` (max 5MB).
- **Backend Storage**: Multer-driven secure storage and metadata management via Mongoose.

---

## 📦 Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React 18, Vite, React Router, Axios |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB, Mongoose |
| **Auth** | JWT, bcryptjs (password hashing) |
| **Styling** | Vanilla CSS (Modern Design System) |
| **File Handling** | Multer |

---

## 🛠️ Step-by-Step Setup Guide

### Prerequisites
- **Node.js**: v18.0.0 or higher ([Download](https://nodejs.org/))
- **MongoDB**: Either local installation ([Download](https://www.mongodb.com/try/download/community)) OR a MongoDB Atlas cloud account.

### Step 1: Install Dependencies
Open your terminal in the project root:

```bash
# Setup Backend
cd server
npm install

# Setup Frontend
cd ../client
npm install
```

### Step 2: Environment Configuration
1. Navigate to the `server` folder.
2. Create a file named `.env` and add:

```env
# MongoDB Connection (Local example)
MONGODB_URI=mongodb://localhost:27017/interview-platform

# JWT Secret (Any random string)
JWT_SECRET=your_secure_random_secret_key

# Ports
PORT=5000
CLIENT_URL=http://localhost:5174
```

### Step 3: Run the Application
You need **two** terminal windows open:

**Terminal 1: Backend**
```bash
cd server
npm run dev
```

**Terminal 2: Frontend**
```bash
cd client
npm run dev
```

---

## 📁 Project Structure

```text
interview/
├── client/                 # React Frontend (Vite)
│   ├── src/
│   │   ├── components/    # UI Building blocks (Header, Buttons)
│   │   ├── context/       # Auth State (JWT)
│   │   ├── pages/         # Views (Landing, Login, Dashboard)
│   │   ├── services/      # API integration (Axios)
│   │   └── styles/        # Global CSS (index.css)
├── server/                 # Express Backend (Node.js)
│   ├── config/            # DB connection logic
│   ├── controllers/       # Business logic (Auth, Resumes)
│   ├── middleware/        # JWT & File filters
│   ├── models/            # Mongoose Schemas (User, Resume)
│   └── routes/            # API Endpoints
└── README.md              # Master Documentation
```

---

## 🛑 Troubleshooting

- **ECONNREFUSED**: Ensure MongoDB service is running locally (`services.msc` on Windows).
- **Port In Use**: Change `PORT` in `.env` or kill processes on 5000/5174.
- **SRV Errors**: If using Atlas, ensure your IP is whitelisted in Atlas Network Access.

---

## 📄 License
This project is licensed under the MIT License.
