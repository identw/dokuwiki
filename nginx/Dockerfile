FROM nginx:1.13.0-alpine
MAINTAINER ilya karataev <ilkarvet89@gmail.com>
ARG useruid
RUN	addgroup -g $useruid nginx-php && \
	adduser -u $useruid -S -s /bin/false -h /var/www/ nginx-php && \
	addgroup nginx-php nginx-php && \
	chown -R nginx-php:nginx-php /var/www

COPY ./default.conf /etc/nginx/conf.d/
COPY ./nginx.conf /etc/nginx/
CMD nginx -g "daemon off;"

