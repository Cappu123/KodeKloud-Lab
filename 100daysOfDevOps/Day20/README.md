# Day 20: Configure Nginx + PHP-FPM Using Unix Sock

## Highlights of today's task

1. Install nginx on `stapp03`(App server3), and configure it to listen on port given(`8093`) in our case, and set document root to `/var/www/html`
2. Install `php-fpm` version, `v-8.2`
3. The `php-fpm` must run via socket given (`/var/run/php-fpm/default.sock`)
4. `php-fpm` and `nginx` must be integrated properly.
5. Finally `curl http://stapp03:8093` should work from the jump host.
