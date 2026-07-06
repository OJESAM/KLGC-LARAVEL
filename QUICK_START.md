# Quick Reference

## Database Credentials
```
Database: your_database_name
User: your_database_user
Password: your_database_password
```

## Getting Started Fast

### 1. Local Development
```bash
# Install dependencies
composer install
npm install

# Setup environment
cp .env.example .env
php artisan key:generate

# Create tables
php artisan migrate

# Load sample data
php artisan db:seed

# Run app
php artisan serve
```

Then visit: `http://localhost:8000`

### 2. Create Test Account
- Go to `/register`
- Fill in name, email, password
- Log in with those credentials

### 3. Test Features
- Home page: `/`
- View devotionals: `/devotionals`
- Submit testimony: `/testimonies/create` (after login)

## File Structure

```
klgc-laravel/
├── app/
│   ├── Http/Controllers/
│   │   ├── Auth/
│   │   ├── DevotionalController.php
│   │   ├── HomeController.php
│   │   └── TestimonyController.php
│   └── Models/
│       ├── User.php
│       ├── Devotional.php
│       ├── Event.php
│       ├── Testimony.php
│       └── ...
├── database/
│   ├── migrations/
│   └── seeders/
├── resources/
│   └── views/
│       ├── auth/
│       ├── devotionals/
│       ├── testimonies/
│       └── layouts/
├── routes/
│   └── web.php
└── README.md
```

## Useful Commands

```bash
# Create migration
php artisan make:migration create_table_name

# Create model
php artisan make:model ModelName

# Run migrations
php artisan migrate

# Seed database
php artisan db:seed

# Clear cache
php artisan cache:clear

# View routes
php artisan route:list
```

## Common Issues

**PHP command not found:**
- Use your hosting provider's terminal or install PHP locally

**Database connection error:**
- Check `.env` file DB credentials and host
- Verify database exists on your server

**Migrations fail:**
- Check database user has CREATE TABLE permission
- Run `php artisan migrate --force` on production

## Support

For Laravel docs: https://laravel.com/docs
For Bootstrap docs: https://getbootstrap.com/docs
