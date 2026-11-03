# LendLoop 📦

> Don't buy it, borrow it.

LendLoop is a campus-focused peer-to-peer web application where students lend and borrow items such as calculators, lab coats, sports gear, textbooks and chargers instead of buying things they need only once.

## Features

- Register and login (JWT authentication)
- Browse items with search, category filter and "Available only" switch
- List your own items
- Send borrow requests with dates and a note to the owner
- Owner can approve or reject requests
- Owner marks an item as returned, and it becomes available again
- Dashboard with My Items, My Requests and Incoming Requests
- Overdue items are flagged automatically

## Tech Stack

- **Frontend:** React, Vite, React Router, Tailwind CSS, Axios
- **Backend:** Node.js, Express, Mongoose, JWT, bcryptjs
- **Database:** MongoDB Atlas

## How to Run

### 1. Requirements
- Node.js v18 or above
- A MongoDB Atlas connection string (or local MongoDB)

### 2. Backend

```bash
cd server
npm install
```

Create `server/.env`:

```ini
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=any_long_random_string
JWT_EXPIRES_IN=7d
CLIENT_URL=http://localhost:5173
```

The MongoDB URL goes in `MONGO_URI`. Example:

```
mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/lendloop?retryWrites=true&w=majority
```

Load demo data (optional), then start the server:

```bash
npm run seed
npm run dev
```

### 3. Frontend

Open a new terminal:

```bash
cd client
npm install
```

Create `client/.env`:

```ini
VITE_API_URL=http://localhost:5000/api
```

```bash
npm run dev
```

Open http://localhost:5173

### Demo login (after seeding)

- Email: `demo1@lendloop.com`
- Password: `password123`
