# KIGC Laravel starter

This folder includes a Bootstrap-based Laravel starter for a church website with:

- Home page
- Devotionals with likes and comments
- Events
- Livestream embed
- Announcements
- Testimonies
- Giving methods cards
- Basic authentication with login and registration

## Setup

1. Copy the files to your hosting server.
2. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```
3. Update your `.env` file with:
   - `APP_KEY` (generate with `php artisan key:generate`)
   - `DB_HOST` (your database host)
   - Database credentials are already filled in
   - Other settings as needed

4. Run migrations:
   ```bash
   php artisan migrate
   ```

5. Start the app:
   ```bash
   php artisan serve
   ```

## Database Details

Your database is configured as:
- Database: `your_database_name`
- User: `your_database_user`
- Tables will be created automatically on first `php artisan migrate`

## Routes

- `/` — Home
- `/register` — Create account
- `/login` — Sign in
- `/devotionals` — All devotionals
- `/testimonies/create` — Submit testimony (auth required)
- `/logout` — Sign out

## Features

- User authentication (login, register, logout)
- Devotionals with likes and comments
- Event listings
- Livestream embeds
- Announcements
- Testimony submissions
- Giving methods payment cards
# KLGC-LARAVEL
