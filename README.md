# 🚀 Laravel API Project (Auth + CRUD + Sanctum)

A complete Laravel backend setup with **authentication, CRUD operations, API development, and Sanctum token-based security**.

---

## 📚 Features

* 🔐 User Authentication (Register / Login / Logout)
* 🔑 Token-based Auth using Laravel Sanctum
* 📦 RESTful API structure
* 🗄️ Database with Eloquent ORM
* 🔄 Full CRUD operations
* 🛡️ Protected routes with middleware

---

## ✅ Prerequisites

* PHP >= 8.1
* Composer
* MySQL / PostgreSQL / SQLite
* Node.js (optional for frontend)

---

## 📦 Installation

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
composer install
cp .env.example .env
php artisan key:generate
```

---

## ⚙️ Environment Setup

Update `.env` file:

```env
APP_NAME=LaravelApp
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_db
DB_USERNAME=root
DB_PASSWORD=
```

---

## 🗄️ Database Setup

```bash
php artisan migrate
```

---

## ▶️ Run the Project

```bash
php artisan serve
```

Server runs at:

```
http://127.0.0.1:8000
```

---

## 🔐 Authentication (Sanctum)

Install Sanctum:

```bash
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate
```

---

## 📡 API Routes

### Auth Routes

```
POST   /api/register
POST   /api/login
GET    /api/me   (Protected)
```

### CRUD Routes (Posts Example)

```
GET    /api/posts
POST   /api/posts
GET    /api/posts/{id}
PUT    /api/posts/{id}
DELETE /api/posts/{id}
```

---

## 🔑 Authentication Flow

1. User registers
2. User logs in → receives token
3. Token is sent in header:

```
Authorization: Bearer YOUR_TOKEN
```

4. Access protected routes

---

## 📁 Project Structure

```
app/
 ├── Http/
 │    ├── Controllers/
 │    └── Middleware/
 ├── Models/

routes/
 ├── web.php
 └── api.php

database/
 └── migrations/

.env
artisan
composer.json
```

---

## 🧪 Testing API

Use tools like:

* Postman
* Thunder Client
* cURL

Example:

```bash
POST /api/login
{
  "email": "test@example.com",
  "password": "password"
}
```

---

## ✅ Best Practices

* 🔒 Never commit `.env`
* 🔑 Use hashed passwords (default in Laravel)
* 🧠 Validate inputs using Form Requests
* 🛡️ Protect routes using middleware
* 📦 Use Eloquent instead of raw SQL

---

## ⚠️ Troubleshooting

**Composer not found**
→ Install Composer and restart terminal

**App key missing**

```bash
php artisan key:generate
```

**Database error**
→ Check `.env` credentials

**Sanctum not working**
→ Run migrations and check middleware

---

## 📌 Future Improvements

* Role-based authentication (Admin/User)
* Email verification
* Password reset
* Rate limiting

---

## 🎉 Ready to Go!

Your Laravel backend API is now fully functional 🚀

---

⭐ If you like this project, give it a star!
