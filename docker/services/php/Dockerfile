FROM php:7.4-fpm-alpine3.12

RUN apk update && apk upgrade && apk add --no-cache \
	bash \
	curl \
	gettext \
	libxml2-dev \
	freetype-dev \
	libpng-dev \
	libjpeg-turbo-dev \
	curl-dev \
	libzip-dev \
	&& docker-php-ext-install -j$(nproc) \
	ctype \
	json \
	pdo \
	pdo_mysql \
	tokenizer \
	xml \
	iconv \
	curl \
	zip \
	&& docker-php-ext-install -j$(nproc) gd \
	&& curl -sS https://getcomposer.org/installer -o composer-setup.php \
	&& php composer-setup.php --install-dir=/usr/local/bin --filename=composer