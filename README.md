# Laravel Project with Role-Based Access Control and Authentication

This project is built on [Laravel](https://laravel.com/), utilizing role-based access control and authentication to manage user permissions efficiently.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Installation

### Prerequisites

- [PHP](https://www.php.net/) >= 7.4
- [Composer](https://getcomposer.org/)
- [Node.js](https://nodejs.org/) and [NPM](https://www.npmjs.com/)

### Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/gautamdheer/mylaravelApp.git
    cd your-repository
    ```

2. Install dependencies:

    ```bash
    composer install
    npm install
    npm run dev
    ```

3. Set up the environment file:

    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

4. Configure your database in the `.env` file:

    ```dotenv
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    ```

5. Run the migrations:

    ```bash
    php artisan migrate
    ```

6. Seed the database (optional but recommended):

    ```bash
    php artisan db:seed
    ```

## Configuration

This project uses [spatie/laravel-permission](https://github.com/spatie/laravel-permission) package for role-based access control. You can publish the configuration file with:

```bash
php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"
