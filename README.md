<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=40&duration=3000&pause=500&color=1F2937&center=true&vCenter=true&width=800&height=120&lines=AutoExpert+%7C+Car+Service+Platform" alt="Typing SVG" />
</p>

## 🚗 AutoExpert - Car Service Booking & Admin Portal

AutoExpert is a Node.js web application built with Express and EJS that provides a car service booking website with user registration/login, service listing, order booking, complaint management, and admin controls.

## 🔥 What AutoExpert Does

- Provides a **public landing page** with car service listings, about page, and contact page.
- Allows users to **register and log in** with secure password hashing.
- Lets users **submit booking orders** for selected services.
- Enables users to **raise complaints** and track their own requests.
- Ships with an **admin dashboard** for managing users, orders, complaints, and services.
- Uses **MongoDB** to persist users, services, orders, and complaints.

## 🎯 Key Features

- **User authentication** with email/password login and JWT token support.
- **User dashboard** for customers.
- **Admin dashboard** with role-protected routes.
- **Service management**: add, update, delete, and list services.
- **Order management**: place orders, view user orders, and admin order control.
- **Complaint management**: create complaints, user complaint list, and admin complaint updates.
- **Dynamic service display** on homepage and service page.
- **Responsive UI** using Bootstrap and EJS views.

## 🧩 Tech Stack

- **Node.js**
- **Express**
- **EJS**
- **MongoDB / Mongoose**
- **bcrypt** for password hashing
- **jsonwebtoken** for auth tokens
- **dotenv** for configuration
- **Multer** for file handling
- **Bootstrap** for frontend styling

## 📁 Main Routes

| Route | Purpose |
|---|---|
| `/` | Homepage with services, about, team, and clients |
| `/about` | About page |
| `/service` | Service listing page |
| `/contact` | Contact page |
| `/login` | User login page |
| `/register` | User registration page |
| `/user/dashboard` | User dashboard |
| `/admin/dashboard` | Admin dashboard |
| `/admin/login` | Admin login page |

## ⚙️ API Endpoints

| Path | Method | Access |
|---|---|---|
| `/register` | POST | Public |
| `/login` | POST | Public |
| `/logout` | GET | Authenticated |
| `/dashboard-stats` | GET | Admin only |
| `/all-users` | GET | Admin only |
| `/orders` | POST | Authenticated |
| `/orders` | GET | Admin only |
| `/user/orders` | GET | Authenticated |
| `/orders/:id` | PUT / DELETE | Admin only |
| `/complaints` | POST | Authenticated |
| `/user/complaints` | GET | Authenticated |
| `/admin/complaints` | GET | Admin only |
| `/complaints/:id` | PUT | Admin only |
| `/services` | POST / GET | Admin only |
| `/services/:id` | PUT / DELETE | Admin only |

## 🛠️ Installation

```bash
cd express-ejs-app
npm install
```

Create a `.env` file in the project root with at least:

```env
MONGO_URI=mongodb://127.0.0.1:27017/carS
JWT_SECRET=your_jwt_secret
PORT=5000
```

## ▶️ Run the App

```bash
<<<<<<< HEAD
node app.js
=======
nodemon app.js
>>>>>>> origin/master
```

Then open:

```text
http://localhost:5000
```

## 🧠 How the App Works

- **Users** can view services and register using the website.
- After login, users can place service orders and submit complaints.
- **Admin users** can access protected admin API routes to review users, track orders, manage service entries, and update complaint statuses.

## 🧭 Project Structure

```text
express-ejs-app/
├── app.js
├── package.json
├── README.md
├── .gitignore
├── config/
│   ├── db.js
│   └── seedAdmin.js
├── controller/
│   └── userController.js
├── middleware/
│   ├── bodyParserMiddleware.js
│   └── checkrole.js
├── models/
│   ├── Admin.js
│   ├── Complaint.js
│   ├── Order.js
│   ├── Service.js
│   └── User.js
├── public/
│   ├── css/
│   ├── images/
│   ├── js/
│   └── data.js
├── routes/
│   └── web.js
└── views/
    ├── about.ejs
    ├── admin-dashboard.ejs
    ├── admin-login.ejs
    ├── contact.ejs
    ├── index.ejs
    ├── login.ejs
    ├── register.ejs
    ├── service.ejs
    ├── user-dashboard.ejs
    └── partials/
        ├── banner.ejs
        ├── footer.ejs
        ├── header.ejs
        ├── hero.ejs
        └── navbar.ejs
```

## 💡 Notes

- The app connects to MongoDB at `mongodb://127.0.0.1:27017/carS` by default.
- Admin-only routes are protected using `checkAdminRole` middleware.
- Passwords are stored securely with `bcrypt` hashing.

## ✅ Summary

AutoExpert is a full-stack Express app for car service bookings, with user authentication, order booking, complaint tracking, and admin service management. It's ideal for showcasing a practical service platform built with Node.js and MongoDB.
