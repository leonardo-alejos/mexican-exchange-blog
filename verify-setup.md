# Mexican Exchange Blog – Setup Verification

## 1. SSH into your server
ssh root@170.64.173.99

## 2. Check Nginx is listening on 80 & 443
sudo ss -tulpn | grep nginx

## 3. Confirm HTTP & HTTPS respond
curl -Ik http://mexican-exchange-blog.site
curl -Ik https://mexican-exchange-blog.site

## 4. Confirm PHP-FPM is running
sudo systemctl status php8.1-fpm

## 5. Confirm MariaDB is running
sudo systemctl status mariadb

## 6. Check DNS from a public resolver
dig +short @8.8.8.8 mexican-exchange-blog.site

## 7. Verify your cron backup script exists
ls -l /opt/scripts/backup_wp.sh

