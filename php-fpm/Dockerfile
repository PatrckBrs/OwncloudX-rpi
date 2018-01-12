# Dockerfile Raspberry Pi Nginx
FROM hypriot/rpi-alpine-scratch:latest

RUN adduser nginx -D -H -u 1000 -s /sbin/nologin

RUN apk update && \
    apk add php7 \
            php7-fpm \
            php7-opcache \
            php7-gd \
            php7-mysqli \
            php7-zlib \
            php7-curl \
            php7-json \
            php7-xml \
            php7-xmlrpc \
            php7-simplexml \
            php7-intl \
            php7-session \
            php7-pdo \
            php7-pdo_mysql \
            php7-dom \
            php7-xmlwriter \
            php7-xmlreader \
            php7-mbstring \
            php7-ctype \
            php7-iconv \
            php7-fileinfo \
            php7-posix \
            php7-pcntl \
            php7-apcu \
            php7-zip

# Set whole bunch of stuff
RUN mkdir -p /run/php

#Remove useless config
RUN rm -rf /etc/php7/php-fpm.d

#Copy special configs
COPY php.ini         /etc/php7/php.ini
COPY php-fpm.conf    /etc/php7/php-fpm.conf

# Ports
EXPOSE 9000

# Boot up Nginx when container is started
CMD ["php-fpm7", "-F"]
