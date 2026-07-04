# Deployment Instructions for KIGC Church Website

## Database Configuration

Your database credentials are:
- **Database:** u289524437_klgc
- **User:** u289524437_klgc
- **Password:** 07na4kZ8p12xU5xK

## Local Setup

1. Install dependencies:
   ```bash
   composer install
   npm install
   ```

2. Copy environment file:
   ```bash
   cp .env.example .env
   ```

3. Generate app key:
   ```bash
   php artisan key:generate
   ```

4. Update `.env` with your database host (ask your hosting provider for the host address).

5. Run migrations to create tables:
   ```bash
   php artisan migrate
   ```

6. (Optional) Seed sample data:
   ```bash
   php artisan db:seed
   ```

7. Build assets:
   ```bash
   npm run build
   ```

## Production Deployment

1. Upload all files to your web server.
2. Create a `.env` file with:
   - `APP_ENV=production`
   - `APP_DEBUG=false`
   - Database credentials (provided above)
   - `APP_KEY` (generate locally and copy over)

3. Run on server:
   ```bash
   php artisan migrate --force
   ```

4. Set proper permissions:
   ```bash
   chmod -R 775 storage bootstrap/cache
   ```

5. Configure your web server to point to the `public/` folder.

## Accessing the App

- Home: `/`
- Register: `/register`
- Login: `/login`
- Devotionals: `/devotionals`
- Share Testimony: `/testimonies/create` (requires login)

## Next Steps

- Add sample content (devotionals, events, announcements)
- Configure email (for verification and notifications)
- Customize branding and colors
- Add more pages as needed
