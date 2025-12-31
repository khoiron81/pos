# Deployment on CWP Pro

Checklist:
- .env (APP_ENV=production, APP_DEBUG=false)
- storage/ writable (storage + bootstrap/cache)
- set correct PHP version (8.2+)
- run:
  php artisan optimize:clear
  php artisan migrate --force
  php artisan db:seed --force

Permissions (typical):
chown -R USER:USER storage bootstrap/cache
chmod -R 775 storage bootstrap/cache