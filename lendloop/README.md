# WorkWala — Local Service Finder

A full stack MERN web application that helps users find and book trusted local service providers such as electricians, plumbers, tutors and cleaners. Service providers can create profiles and manage their services.

## Problem Statement

Many people struggle to find reliable local services quickly, and small service providers lack an online platform to promote their work. WorkWala gives both sides one place: users search, filter and book, and providers list and manage their services.

## Features

**Users**
- Signup and login
- Search and filter service providers by category and location
- View provider profiles, book services, leave reviews

**Service providers**
- Create a service profile
- Add, update and delete services
- Manage bookings

## Tech Stack

- **Frontend:** React, Vite, Tailwind CSS, React Router, Axios
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose)
- **Auth:** JWT + bcrypt

## How to Run

### 1. Requirements
- Node.js v18 or above
- A MongoDB Atlas connection string (or local MongoDB)

### 2. Install

```bash
npm run install-all
```

### 3. Create `server/.env`

```ini
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=any_long_random_string
```

The MongoDB URL goes in `MONGODB_URI`. Example:

```
mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/workwala?retryWrites=true&w=majority
```

### 4. Start

```bash
npm run dev
```

- Frontend: http://localhost:5173
- Backend: http://localhost:5000
- Health check: http://localhost:5000/api/health
