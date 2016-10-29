FROM ubuntu:latest
MAINTAINER Moon_Yue "luna825"
ENV REFRESHED_AT 2016-10-29
RUN apt-get update && apt-get -y install nginx
RUN mkdir -p /var/www/html/website
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80