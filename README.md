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

## 🛠 Getting Started

1. Clone the repository

    git clone https://github.com/yourname/ci-php-docker-stack.git
    cd ci-php-docker-stack

2. Start the containers

    docker-compose up -d --build

🌐 Access URLs

    Service	URL
    App	http://localhost:8080
    phpMyAdmin	http://localhost:8081

🔐 Default Credentials

    Component	  Username	Password
    MariaDB	    ci_user	  ci_password
    phpMyAdmin	ci_user or root	ci_password or root_password

🧩 Restore Database using phpMyAdmin

    You can easily import a .sql file into MariaDB using the phpMyAdmin interface:

    Open http://localhost:8081 in your browser.

    Log in using the credentials above.

    Select the database ci_db from the left panel.

    Click the Import tab.

    Choose your .sql file under "File to import".

    Click Go to execute the import.

⚙️ Composer
    During build, composer update is automatically run inside the /var/www/html/ams directory.

    To manually run Composer in the container:

    docker exec -it ci_php_app bash
    cd /var/www/html/ams
    composer update

🧪 Useful Commands

    # Rebuild everything from scratch
    docker-compose down -v
    docker-compose up -d --build

# Login to containers
    docker exec -it ci_php_app bash
    docker exec -it mariadb mysql -u root -p
