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

![Architecture](./domain-platform-structure.png)

---

## 🗄️ Database Design

```mermaid
erDiagram

    USERS {
        int id PK
        string name
        string email
        string phone
        string role
    }

    ORDERS {
        int id PK
        int user_id FK
        float total_amount
        string status
        string payment_reference
    }

    ORDER_ITEMS {
        int id PK
        int order_id FK
        string domain
        string type
        int years
        float price
    }

    DOMAINS {
        int id PK
        int user_id FK
        int order_id FK
        string full_domain
        string domain_name
        string extension
        float purchase_price
        date expiry_date
        string status
    }

    DOMAIN_EXTENSIONS {
        int id PK
        string extension
        float price
        float renewal_price
        string is_active
    }

    DOMAIN_LOCKS {
        int id PK
        string domain
        int user_id FK
        string expires_at
    }

    PAGES {
        int id PK
        string slug
        string title
    }

    PAGE_SECTIONS {
        int id PK
        int page_id FK
        string type
        string content
        int order
    }

    CONTACT_MESSAGES {
        int id PK
        string name
        string email
        string subject
        string message
    }

    USERS ||--o{ ORDERS : places
    USERS ||--o{ DOMAINS : owns
    USERS ||--o{ DOMAIN_LOCKS : locks

    ORDERS ||--o{ ORDER_ITEMS : contains
    ORDERS ||--o{ DOMAINS : creates

    PAGES ||--o{ PAGE_SECTIONS : has
```
---


# 📸 Screenshots

---

## 🟢 User Frontend

### 🔍 Domain Search and Home Page
![Home](./screenshots/frontend/home.png)

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

This project was built to simulate a real-world domain marketplace and helped me move beyond basic CRUD development into solving actual engineering problems.

While building this system, I focused on handling practical challenges like concurrency (domain locking during checkout), external API integration, and maintaining data consistency across the order and payment flow. I also worked on structuring the backend in a scalable way using services, queues, and caching.

On the frontend side, I aimed to keep the experience simple and functional, making it easy for users to search, purchase, and manage domains, while also building an admin panel to monitor and control the system.

Overall, this project reflects my approach as a developer — not just writing code, but thinking about reliability, edge cases, and how a system behaves in real scenarios.

