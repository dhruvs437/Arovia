# Arovia Monorepo

Arovia is a modern full-stack application built with a **Next.js frontend** and a **Node.js + Express backend**. It features advanced caching, AI integration, secure authentication, and scalable architecture for production-ready deployments.

---

## 📂 Project Structure

arovia/ 
├── frontend/              # Next.js frontend application 
│   ├── src/               # Frontend source code 
│   ├── public/            # Static assets 
│   ├── .env.local         # Frontend environment variables 
│   └── README.md          # Frontend documentation 
│ ├── backend/               # Node.js + Express API server 
│   ├── src/               # Backend source code 
│   ├── dist/              # Compiled JavaScript 
│   ├── .env               # Backend environment variables 
│   └── README.md          # Backend documentation 
│ ├── package.json           # Root package (if using workspaces or scripts) 
└── README.md              # Monorepo documentation


---

## 🚀 Tech Stack

### Frontend
- Next.js 13+ with TypeScript
- React 18
- TailwindCSS (or preferred UI framework)
- SWR (stale-while-revalidate fetching)
- Axios/Fetch API for backend consumption
- ESLint + Prettier for code quality

### Backend
- Node.js 18+ with TypeScript
- Express.js with async error handling
- MongoDB with Mongoose
- Redis with ioredis
- AI integration via Groq SDK
- JWT authentication with refresh tokens
- Zod validation
- Pino logging
- Rate limiting with Redis
- Cheerio for Web Scraping

---

## 📋 Prerequisites

Before running this project, ensure you have:

- Node.js 18+
- MongoDB (local or cloud instance)
- Redis server
- npm or yarn

---

## 🛠️ Installation

Clone the repository and navigate:



git clone  
cd arovia

Install dependencies in both apps:
cd frontend && npm install 
cd ../backend && npm install


---

## 🔧 Environment Configuration

### Frontend (`frontend/.env.local`)

NEXT_PUBLIC_API_URL=http://localhost:5000/api/v1
NEXT_PUBLIC_ENV=development


### Backend (`backend/.env`)

Server Configuration
NODE_ENV=development PORT=5000 API_VERSION=v1
Database
MONGODB_URI=mongodb://localhost:27017/arovia MONGODB_TEST_URI=mongodb://localhost:27017/arovia-test
Redis Cache
REDIS_URL=redis://localhost:6379 REDIS_PASSWORD=your_redis_password
JWT Authentication
JWT_SECRET=your-super-secret-jwt-key JWT_EXPIRES_IN=7d JWT_REFRESH_SECRET=your-refresh-secret JWT_REFRESH_EXPIRES_IN=30d
Groq AI
GROQ_API_KEY=your_groq_api_key GROQ_MODEL=mixtral-8x7b-32768
Rate Limiting
RATE_LIMIT_WINDOW_MS=900000 RATE_LIMIT_MAX_REQUESTS=100
CORS
ALLOWED_ORIGINS=http://localhost:3000,https://your-frontend-domain.com
Encryption
BCRYPT_SALT_ROUNDS=12
Logging
LOG_LEVEL=info


---

## 🚦 Getting Started

### Start Backend

cd backend 
npm run dev

Runs at: `http://localhost:5000`

### Start Frontend
(Open another terminal)

cd frontend 
npm run dev

Runs at: `http://localhost:3000`

---

## 🚀 Deployment

- Use **PM2** or Docker for backend process management.
- Deploy frontend via **Vercel/Netlify** or any static hosting.
- Configure proper **CORS origins** in backend `.env`.

---

## 📊 Features

- **Frontend**
  - Modern Next.js SPA/SSR support
  - API integration with backend
  - Responsive UI
  - SWR caching for client-side data fetching

- **Backend**
  - RESTful API with Express
  - MongoDB & Redis integration
  - AI-powered features with Groq
  - Secure JWT authentication
  - Zod-based validation
  - Centralized logging and error handling

---

## 🧪 API Endpoints (Backend)

- **Auth**
  - `POST /api/v1/auth/register`
  - `POST /api/v1/auth/login`
  - `POST /api/v1/auth/refresh`
  - `POST /api/v1/auth/logout`

- **Health**
  - `GET /api/v1/health`
  - `GET /api/v1/health/detailed`

---

## 🤝 Contributing

1. Fork this repo  
2. Create a feature branch (`git checkout -b feature/new-feature`)  
3. Commit your changes (`git commit -m 'feat: Add new feature'`)  
4. Push to branch (`git push origin feature/new-feature`)  
5. Open a PR  

---

## 📝 License

This project is private and proprietary.  



