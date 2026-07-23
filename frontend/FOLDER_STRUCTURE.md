# PhotoHub — Folder Structure

```
PhotoHub/
├── database/
│   ├── 01_schema.sql
│   ├── 02_seed_data.sql
│   └── README.md
├── public/
│   ├── icons/
│   ├── images/
│   ├── videos/
│   └── favicon.ico
├── src/
│   ├── assets/
│   │   ├── fonts/
│   │   ├── icons/
│   │   ├── images/
│   │   └── logos/
│   ├── components/
│   │   ├── cards/
│   │   ├── chatbot/
│   │   │   └── ChatWidget.jsx
│   │   ├── common/
│   │   │   ├── Badge.jsx
│   │   │   ├── EmptyState.jsx
│   │   │   ├── Loader.jsx
│   │   │   ├── Logo.jsx
│   │   │   └── RatingStars.jsx
│   │   ├── dashboard/
│   │   │   └── StatCard.jsx
│   │   ├── footer/
│   │   │   └── Footer.jsx
│   │   ├── forms/
│   │   │   ├── Input.jsx
│   │   │   ├── Select.jsx
│   │   │   └── Textarea.jsx
│   │   ├── modals/
│   │   │   └── ConfirmModal.jsx
│   │   ├── navbar/
│   │   │   └── Navbar.jsx
│   │   ├── notifications/
│   │   │   └── ToastHost.jsx
│   │   ├── sidebar/
│   │   │   └── Sidebar.jsx
│   │   ├── tables/
│   │   │   └── DataTable.jsx
│   │   └── ui/
│   │       ├── Card.jsx
│   │       ├── Modal.jsx
│   │       └── StatPill.jsx
│   ├── constants/
│   │   └── index.js
│   ├── context/
│   │   ├── AuthContext.jsx
│   │   └── ToastContext.jsx
│   ├── data/
│   │   └── mockData.js
│   ├── hooks/
│   ├── layouts/
│   │   ├── AdminLayout.jsx
│   │   ├── AuthLayout.jsx
│   │   ├── CustomerLayout.jsx
│   │   ├── DashboardLayout.jsx
│   │   ├── PhotographerLayout.jsx
│   │   └── PublicLayout.jsx
│   ├── pages/
│   │   ├── admin/
│   │   │   ├── Approvals.jsx
│   │   │   ├── Bookings.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Logs.jsx
│   │   │   ├── PaymentIssues.jsx
│   │   │   ├── Payments.jsx
│   │   │   ├── Photographers.jsx
│   │   │   ├── Refunds.jsx
│   │   │   ├── Reports.jsx
│   │   │   ├── Settings.jsx
│   │   │   └── Users.jsx
│   │   ├── auth/
│   │   │   ├── ForgotPassword.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   └── ResetPassword.jsx
│   │   ├── customer/
│   │   │   ├── BookingDetails.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── EditProfile.jsx
│   │   │   ├── MyBookings.jsx
│   │   │   ├── PaymentHistory.jsx
│   │   │   ├── Profile.jsx
│   │   │   └── Reviews.jsx
│   │   ├── errors/
│   │   │   ├── NotFound.jsx
│   │   │   ├── ServerError.jsx
│   │   │   └── Unauthorized.jsx
│   │   ├── photographer/
│   │   │   ├── AddPackage.jsx
│   │   │   ├── AddPortfolio.jsx
│   │   │   ├── BookingRequests.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Earnings.jsx
│   │   │   ├── Packages.jsx
│   │   │   ├── Portfolio.jsx
│   │   │   └── Profile.jsx
│   │   └── public/
│   │       ├── AboutPage.jsx
│   │       ├── ContactPage.jsx
│   │       ├── FaqPage.jsx
│   │       ├── HomePage.jsx
│   │       ├── PackageDetails.jsx
│   │       ├── PackagesPage.jsx
│   │       ├── PhotographerDetails.jsx
│   │       ├── PhotographerList.jsx
│   │       ├── PortfolioPage.jsx
│   │       └── SearchPage.jsx
│   ├── routes/
│   │   └── ProtectedRoute.jsx
│   ├── services/
│   │   ├── _demoMode.js
│   │   ├── adminService.js
│   │   ├── authService.js
│   │   ├── bookingService.js
│   │   ├── packageService.js
│   │   ├── paymentService.js
│   │   ├── photographerService.js
│   │   ├── portfolioService.js
│   │   ├── refundService.js
│   │   ├── reviewService.js
│   │   └── userService.js
│   ├── utils/
│   │   ├── api.js
│   │   └── helpers.js
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .env.example
├── .gitignore
├── README.md
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
└── vite.config.js
```

**150 files** across the tree above. Empty folders (`assets/*`, `hooks/`,
`components/cards/`, `public/icons`, `public/images`, `public/videos`) are
kept in git via `.gitkeep` placeholders so the directory layout is preserved
even before real assets/hooks are added.
