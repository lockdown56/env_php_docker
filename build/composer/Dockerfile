FROM lockdown56-docker.pkg.coding.net/registry/public/php:7.4.0-cli-1

ADD composer /usr/bin/composer
RUN chmod +x /usr/bin/composer \
    && rm /etc/apt/preferences.d/no-debian-php \
    && apt-get update \
    && apt-get install -y apt-utils git zip unzip php-zip 


WORKDIR /app
