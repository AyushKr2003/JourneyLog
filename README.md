# JourneyLog

A full-stack tourism and travel blogging platform designed for sharing travel experiences across Indonesia. JourneyLog features multi-role user authentication, category-based article organization, and user profile management.

---

## 🚀 Tech Stack & Requirements

- **Backend**: PHP 7.4 / 8.0, Laravel 7.x
- **Frontend**: Blade Templating, Bootstrap 4, Bootstrap Icons
- **Database**: SQLite (default) / MySQL
- **Storage**: Laravel File Storage (linked to public directory)

---

## 🛠️ Quick Start (Running via Docker)

Since Laravel 7 requires PHP 7.4/8.0, the easiest way to run the application is using Docker:

```bash
docker run --rm -it -p 8001:8000 -v $(pwd):/app -w /app php:7.4-cli php artisan serve --host=0.0.0.0 --port=8000
```
Open [http://localhost:8001](http://localhost:8001) in your browser.

---

## 🔑 Demo Accounts

| Role | Email | Password |
| :--- | :--- | :--- |
| **Admin** | `admin@google.com` | `adminadmin` |
| **User A** | `user_a@google.com` | `useruser` |
| **User B** | `user_b@google.com` | `useruser` |

---

## 💻 Manual Setup

1. **Install Dependencies**:
   ```bash
   composer install
   ```
2. **Environment & Key Setup**:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
3. **Storage Linking**:
   ```bash
   php artisan storage:link
   ```
4. **Database Migration & Seeding**:
   ```bash
   touch database/database.sqlite
   php artisan migrate:fresh --seed
   ```
5. **Run Local Server**:
   ```bash
   php artisan serve
   ```

---

## ✨ Features

- **Role-Based Access Control**: Distinguishes between Admin operations and standard user capabilities.
- **Category Filtering**: Filter articles by exclusive travel categories and region destinations.
- **Article CRUD & Image Uploads**: Create, read, and delete travel posts with embedded photo uploads.
- **Profile Management**: Customize user profile details and view personal blog posts.
