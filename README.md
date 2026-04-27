# 🚀 Domain Marketplace Platform

## 📌 Overview
A full-stack domain marketplace platform inspired by GoDaddy, built with a production-oriented architecture and real-world system design principles.

The platform allows users to search, purchase, and manage domains while ensuring secure checkout using concurrency control mechanisms. It also includes an admin dashboard for complete system monitoring and management.

---

## ⚙️ Tech Stack

- Backend: Laravel (Service Layer, Queues, Caching)
- Frontend: Vue 3 (User Interface)
- Admin Panel: Vue 3 (Admin Dashboard)
- Database: MySQL
- Authentication: Laravel Sanctum
- Caching & Queues: Redis
- External API: ResellerClub (Domain availability)

---

# 🧠 System Breakdown

---

## 🔧 Backend (Laravel API)

Designed using a clean and scalable architecture with separation of concerns.

### Key Features:
- Domain search via external API
- Secure checkout with domain locking (prevents double purchase)
- Order & payment flow handling
- Domain purchase and renewal lifecycle
- Queue-based background jobs
- Caching for performance optimization
- Logging & error handling

### Highlights:
- Concurrency-safe checkout system
- External API integration with retry handling
- Queue-based async processing
- Scalable service-based architecture

---

## 🌐 User Frontend (Vue 3)

Provides a smooth and interactive user experience for domain discovery and management.

### Features:
- Real-time domain search with availability & pricing
- Multi-domain checkout flow
- User dashboard (domains, expiry, renewals)
- Secure authentication (Sanctum)
- Clean and responsive UI

---

## 📊 Admin Panel (Vue 3)

Centralized control panel for managing platform operations.

### Features:
- User management
- Domain management
- Order tracking (paid, pending, failed)
- Revenue analytics dashboard
- Extension & pricing configuration

---

# 🏗️ Architecture

![Architecture](./architecture.png)

---

# 📸 Screenshots

---

## 🟢 User Frontend

### 🏠 Home Page
![Home](./screenshots/frontend/home.png)

### 🔍 Domain Search
![Search](./screenshots/frontend/home.png)

### 🛒 Cart
![Cart](./screenshots/frontend/cart.png)

### 💳 Checkout
![Checkout](./screenshots/frontend/checkout.png)

### 📊 User Domains Dashboard
![User Dashboard](./screenshots/frontend/dashboard-domains.png)

### 📦 User Orders Dashboard
![Orders](./screenshots/frontend/dashbboard-orders.png)

### 🔐 Login
![Login](./screenshots/frontend/login.png)

### 📧 Order Receipt Email
![Receipt](./screenshots/frontend/reciept-mail.png)

---

## 🔵 Admin Panel

### 📊 Dashboard
![Admin Dashboard](./screenshots/admin/dashboard.png)

### 👥 Users
![Users](./screenshots/admin/users.png)

### 🌐 Domains
![Domains](./screenshots/admin/domains.png)

### 🧾 Pages Management
![Pages](./screenshots/admin/pages.png)

### ⚙️ Settings
![Settings](./screenshots/admin/settings.png)

### 🧩 Domain Extensions
![Extensions](./screenshots/admin/domain-extensions.png)

### 👤 Profile
![Profile](./screenshots/admin/profile.png)

### 🔐 Admin Login
![Admin Login](./screenshots/admin/login.png)

---

# 🔗 Repositories

- 🔧 Backend API  
  https://github.com/Maninder2002/domain-platform-backend/

- 🌐 User Frontend  
  https://github.com/Maninder2002/domain-platform-frontend/

- 📊 Admin Panel  
  https://github.com/Maninder2002/domain-platform-admin-frontend/

---

# 🔥 Key Engineering Highlights

- Service-based backend architecture
- Concurrency-safe checkout using domain locking
- External API integration with caching and retry logic
- Queue-based asynchronous processing
- Clean and scalable system design
- Production-ready error handling and logging

---

# 🎯 Conclusion

This project demonstrates strong backend engineering skills, system design thinking, and the ability to build scalable, real-world applications using modern technologies.

