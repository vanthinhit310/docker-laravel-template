FROM php:8.2-fpm-alpine

RUN docker-php-ext-install pdo pdo_mysql \
    && docker-php-ext-install bcmath \
    && apk update \ 
    && apk add --no-cache supervisor

RUN mkdir -p /etc/supervisor/logs

COPY supervisord.conf /etc/supervisor/supervisord.conf

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/supervisord.conf"]