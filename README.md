# ci-php-docker-stack
🐳 A complete Docker-based development stack for PHP 8.2 CI projects with MariaDB, phpMyAdmin, Composer, Apache, and automatic dependency installation. Designed for easy local development with persistent database storage and support for .htaccess URL rewriting.

# CI PHP Docker Stack

A ready-to-run Docker setup for continuous integration (CI) projects using PHP 8.2, MariaDB, and phpMyAdmin. Built with Composer, Apache, and support for `.htaccess` rewrites, this stack is ideal for local development and testing environments.

## Features

- ✅ PHP 8.2 with Apache
- 🐬 MariaDB 10.11 with persistent volume
- 🧩 phpMyAdmin for easy DB access
- 📦 Composer support for automatic dependency management
- 🔁 `.htaccess` support with mod_rewrite enabled
- 🗂 Live code reloading via volume mounts

## Getting Started

```bash
git clone https://github.com/yourname/ci-php-docker-stack.git
cd ci-php-docker-stack
docker-compose up -d --build
