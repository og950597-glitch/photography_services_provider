# PhotoHub — Photography Booking & Management System

A React + Tailwind CSS (JavaScript, no TypeScript) frontend for a
photography booking platform, modeled directly on an ER diagram covering
Users, Photographers, Admins, Packages, Portfolio, Bookings, Reviews,
Payments, Refunds, Payment Issues, and System Logs.

## ✨ Features

- **Public site** — home, about, contact, FAQ, photographer search/listing,
  photographer details, packages
- **Auth** — login, register, forgot/reset password
- **Customer dashboard** — bookings, booking details, payment history,
  reviews, profile
- **Photographer dashboard** — bookings, packages, portfolio, earnings,
  profile
- **Admin dashboard** — users, photographers, bookings, payments, refunds,
  payment issues, approvals, reports, logs, settings
- **Bundled demo data** so the entire UI is clickable with zero backend setup
- **MySQL schema + seed data** ready to plug in a real API

## 📁 Folder Structure

```
PhotoHub/
├── database/              ← MySQL schema + seed data
│   ├── 01_schema.sql
│   ├── 02_seed_data.sql
│   └── README.md
├── public/                ← static assets (icons, images, videos, favicon)
├── src/
│   ├── assets/             ← fonts, icons, images, logos
│   ├── components/         ← navbar, footer, sidebar, forms, tables,
│   │                          modals, dashboard widgets, chatbot, ui kit
│   ├── constants/          ← app-wide constants
│   ├── context/            ← AuthContext, ToastContext
│   ├── data/mockData.js    ← demo data mirroring the MySQL seed
│   ├── hooks/               ← custom React hooks
│   ├── layouts/             ← Public, Auth, Dashboard, Admin, Customer,
│   │                           Photographer layouts
│   ├── pages/
│   │   ├── public/          ← Home, About, Contact, FAQ, Search, ...
│   │   ├── auth/             ← Login, Register, Forgot/Reset Password
│   │   ├── customer/         ← Dashboard, bookings, payments, reviews
│   │   ├── photographer/     ← Dashboard, packages, portfolio, earnings
│   │   ├── admin/            ← Dashboard, users, approvals, refunds, logs
│   │   └── errors/           ← 404 / 403 / 500
│   ├── routes/               ← ProtectedRoute
│   ├── services/             ← one file per ER-diagram entity
│   ├── utils/                ← api client, helpers
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── .env.example
├── package.json
├── tailwind.config.js
└── vite.config.js
```

See [`FOLDER_STRUCTURE.md`](./FOLDER_STRUCTURE.md) for the complete,
file-by-file tree.

## 🚀 Getting Started

### 1. Run the frontend

```bash
cd PhotoHub
npm install
npm run dev
```

Open the printed local URL (usually `http://localhost:5173`).

The app works immediately with **bundled demo data** — no backend required
to click around. Log in with any of these (any password works in demo
mode):

| Role         | Email                     |
|--------------|---------------------------|
| Client       | riya.sharma@example.com   |
| Photographer | devansh.rao@example.com   |
| Admin        | anita.desai@example.com   |

### 2. Set up the MySQL database

```bash
mysql -u root -p < database/01_schema.sql
mysql -u root -p < database/02_seed_data.sql
```

This creates `photohub_db` with all 11 tables from the ER diagram, fully
seeded with sample clients, photographers, an admin, bookings, payments,
refunds, payment issues, reviews, portfolio items, and packages. See
[`database/README.md`](./database/README.md) for details and login
credentials.

### 3. Connect the frontend to a real backend

The frontend talks to a REST API defined by `VITE_API_BASE_URL` (copy
`.env.example` to `.env`). Every file in `src/services/` calls that API
first and only falls back to the bundled mock data if the request fails —
so once you build a backend (Node/Express, Laravel, Spring Boot, etc.) on
top of the MySQL database and point `VITE_API_BASE_URL` at it, the whole
app switches to live data with no other code changes needed.

Expected REST shape (adjust to your backend):

- `POST /auth/login`, `POST /auth/register`
- `GET/PUT /users`, `GET/PATCH /users/:id/status`
- `GET/POST/PUT /photographers`, `PATCH /photographers/:id/verify`
- `GET/POST/PUT/DELETE /packages`
- `GET/POST/DELETE /portfolio`
- `GET/POST/PATCH /bookings`
- `GET/POST /reviews`
- `GET/POST/PATCH /payments`
- `GET/POST/PATCH /refunds`
- `GET /admin/stats`, `GET/PATCH /admin/payment-issues`, `GET /admin/logs`

## 🛠️ Tech Stack

- **React 18** (JavaScript, `.jsx`)
- **React Router v6**
- **Tailwind CSS** (custom "PhotoHub" theme: ink / paper / brass / teal)
- **Vite**
- **MySQL** for the database layer

## 🎨 Design

A photography-brand palette (charcoal ink, warm paper, brass/gold accent,
deep teal) with an aperture-blade mark used as the recurring signature motif
across the navbar, hero, and auth screens.

## 📦 Available Scripts

| Command           | Description                       |
|--------------------|------------------------------------|
| `npm run dev`      | Start the Vite dev server          |
| `npm run build`    | Build for production               |
| `npm run preview`  | Preview the production build       |
| `npm run lint`     | Run ESLint                         |

## 🤝 Contributing

1. Fork the repo and create a feature branch
2. Make your changes
3. Open a pull request with a clear description of what changed and why

## 📄 License

Add your license of choice here (e.g. MIT).
