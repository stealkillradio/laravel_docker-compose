FROM php:7.1-fpm

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN apt-get update && apt-get install -y \
        libxml2-dev \
	libfreetype6-dev \
	libjpeg62-turbo-dev \
	libjpeg-dev \
	libpq-dev \
	libmemcached-dev \
	curl \
	zip \
	git

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install mbstring mysqli gd pdo_mysql pdo_pgsql soap xml zip
#RUN docker-php-ext-enable memcached
#RUN echo "ini_set('display_errors', 'Off');" >> /usr/local/etc/php-fpm.conf

RUN curl -sS https://getcomposer.org/installer -o composer-setup.php \
	&& php composer-setup.php --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]
