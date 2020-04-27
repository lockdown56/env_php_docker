FROM lockdown56-docker.pkg.coding.net/registry/public/php:7.4.0-cli-2

ADD composer /usr/bin/composer
COPY sources.list /etc/apt/sources.list
RUN chmod +x /usr/bin/composer \
    && composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/ \
    && mkdir /.composer \
    && rm /etc/apt/preferences.d/no-debian-php \
    && apt-get update \
    && apt-get install -y apt-utils git zip unzip php-zip 


WORKDIR /app
