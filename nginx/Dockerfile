FROM nginx:stable-alpine

ARG NGINXGROUP
ARG NGINXUSER

ENV NGINXGROUP=www-data
ENV NGINXUSER=www-data

RUN sed -i "s/user www-data/user ${NGINXUSER}/g" /etc/nginx/nginx.conf

ADD ./default.conf /etc/nginx/conf.d/

RUN mkdir -p /var/www/html

RUN adduser -g ${NGINXGROUP} -s /bin/sh -D ${NGINXUSER}; exit 0
