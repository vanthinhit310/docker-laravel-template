FROM php:8.2-fpm

ADD supervisord.conf /etc/

RUN apt-get update \ 
    && apt-get install -y --no-install-recommends supervisor

CMD ["supervisord", "-c", "/etc/supervisord.conf"]