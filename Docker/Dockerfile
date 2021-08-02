FROM newdeveloper/apache-php:latest

# Corrige os avisos do debconf no build
ARG DEBIAN_FRONTEND=noninteractive

# Instala extensões selecionadas e outras coisas
RUN apt-get update && apt-get install-y \
    php7.4-mysql \
    php7.4-bcmath \
    php7.4-gd \
    php7.4-imap \
    php-yaml \
    vim \
    && docker-php-ext-install -j$(nproc) iconv mcrypt \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd\
    && docker-php-ext-install mbstring \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/* /var/www/html/*

WORKDIR "/application"
