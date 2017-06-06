FROM php:7-fpm-alpine
MAINTAINER ilya karataev <ilkarvet89@gmail.com>
ARG useruid 
RUN	addgroup -g $useruid nginx-php && \
	adduser -u $useruid -S -s /bin/false -h /var/www/ nginx-php && \
	addgroup nginx-php nginx-php && \
	chown -R nginx-php:nginx-php /var/www
COPY ./www.conf /usr/local/etc/php-fpm.d/
WORKDIR /var/www
CMD ["php-fpm"]
