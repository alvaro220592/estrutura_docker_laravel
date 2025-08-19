FROM php:8.3-fpm-alpine

# Instalar dependências do sistema
RUN apk add --no-cache \
    bash git unzip curl nodejs npm \
    libzip-dev sqlite sqlite-dev oniguruma-dev

# Instalar extensões do PHP
RUN docker-php-ext-install pdo pdo_sqlite pdo_mysql zip mbstring

# Instalar Composer
RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

WORKDIR /var/www/html