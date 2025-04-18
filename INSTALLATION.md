# Bhartiya Shiksha Board Website - Installation Guide

This guide will help you set up and run the Bhartiya Shiksha Board Laravel project locally.

## Prerequisites

- PHP >= 8.1
- Composer
- MySQL or compatible database
- Web server (optional, Laravel's built-in server can be used)
- Node.js and npm (optional, for frontend asset compilation)

## Steps to Install and Run

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install PHP dependencies**

   ```bash
   composer install
   ```

3. **Set up environment file**

   Copy the example environment file and configure your database credentials:

   ```bash
   cp .env.example .env
   ```

   Edit `.env` and update the following variables:

   ```
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=bsb_database
   DB_USERNAME=root
   DB_PASSWORD=your_password
   ```

4. **Generate application key**

   ```bash
   php artisan key:generate
   ```

5. **Run database migrations**

   ```bash
   php artisan migrate
   ```

6. **Seed the database with admin user**

   ```bash
   php artisan db:seed --class=AdminUserSeeder
   ```

7. **Run the development server**

   ```bash
   php artisan serve
   ```

8. **Access the application**

   Open your browser and go to:

   ```
   http://localhost:8000/login
   ```

   Use the following admin credentials to log in:

   - Email: admin@mail.com
   - Password: Admin@1234

## Additional Notes

- To customize the frontend assets, you may need to install Node.js dependencies and compile assets using Laravel Mix or Vite.
- For production deployment, configure a proper web server like Apache or Nginx and set up environment variables accordingly.

## Troubleshooting

- Ensure your PHP version meets the minimum requirement.
- Check database connection settings if migrations fail.
- Run `php artisan config:cache` if environment variables are not loading correctly.

---

This completes the installation and setup of the Bhartiya Shiksha Board website project.
