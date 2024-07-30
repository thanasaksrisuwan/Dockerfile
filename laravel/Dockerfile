FROM webdevops/php-nginx:8.2-alpine

COPY ./laravel/php.ini /opt/docker/etc/php/php.ini
COPY ./laravel/vhost.conf /opt/docker/etc/nginx/vhost.conf
COPY composer.json composer.lock /app/
RUN composer install --no-interaction --no-scripts --no-suggest
COPY . /app