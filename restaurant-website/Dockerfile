# Étape de construction
FROM php:8.3-fpm AS builder

WORKDIR /app

# Installation des dépendances PHP
RUN apt-get update && apt-get install -y \
    unzip \
    libpq-dev \
    && docker-php-ext-install pdo pdo_pgsql

# Installation de Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

COPY . .


# Changer le propriétaire des fichiers pour www-data
RUN chown -R www-data:www-data /app

# Commande par défaut pour exécuter PHP-FPM en premier plan
CMD ["php-fpm"]