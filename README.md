Got it! Here’s the **fully updated `README.md`** with **Tailwind CSS**, **Docker setup**, and **multi-domain routing** (admin.localhost:8080 / localhost:8080):

---

# 🛍️ E-Commerce Laravel App

**Modern e-commerce platform** built with Laravel, Tailwind CSS, and Docker. Features separate admin/user interfaces, cart system, and order management.

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

## ✨ Features

- **Multi-domain routing**:
  - `localhost:8080` → User storefront
  - `admin.localhost:8080` → Admin dashboard
- **Modern UI** with Tailwind CSS
- **Dockerized** for easy setup
- **Admin features**:
  - Product/category management
  - Order fulfillment
- **User features**:
  - Cart/checkout system
  - Order history

## 🛠️ Tech Stack

- **Backend**: Laravel 10
- **Frontend**: Tailwind CSS, Blade
- **Database**: SQLite
- **Infrastructure**: Docker

## 🐳 Docker Setup (Recommended)

### Prerequisites

- Docker & Docker Compose

### Run in 3 Steps

1. **Clone and configure**:

   ```sh
   git clone https://github.com/mohamedabdellhay/ecommerce-laravel-app.git
   cd ecommerce-laravel-app
   cp .env.example .env
   ```

2. **Start containers**:

   ```sh
   docker-compose up -d
   ```

3. **Run setup commands**:
   ```sh
   docker-compose exec app php artisan key:generate
   docker-compose exec app php artisan migrate --seed
   ```

▶ **Access the apps**:

- User Interface: http://localhost:8080
- Admin Interface: http://admin.localhost:8080

## 🖥️ Manual Setup (Without Docker)

1. Install PHP 8.1+, SQLite
2. Configure `.env` for SQLite:
   ```env
   DB_CONNECTION=sqlite
   DB_DATABASE=/absolute/path/to/database.sqlite
   ```
3. Run:
   ```sh
   composer install
   touch database/database.sqlite
   php artisan migrate --seed
   php artisan serve
   ```

## 🌟 Tailwind CSS Workflow

If making frontend changes:

```sh
# Watch for changes (inside Docker)
docker-compose exec app npm run dev

# Or rebuild (production)
docker-compose exec app npm run build
```

---

### Key Improvements:

1. **Docker-first approach** with clear commands
2. **Multi-domain routing** documentation
3. **Tailwind CSS** workflow section
4. Badges reflect the actual stack
