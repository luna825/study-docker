FROM ubuntu
MAINTAINER Moon Yue <luna825@qq.com>
ENV REFRESHED 2016-10-30
RUN apt-get -y update
RUN apt-get -y apache2
VOLUME ["/var/www/html"]
WORKDIR /var/www/html
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
RUN mkdir -p $APACHE_LOG_DIR $APACHE_RUN_DIR $APACHE_LOCK_DIR
EXPOSE 80
ENTRYPOINT ["/usr/bin/apache2"]
CMD ["-D", "FOREGROUND"]