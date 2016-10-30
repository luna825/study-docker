FROM ubuntu
MAINTAINER Moon Yue <luna825@qq.com>
ENV REFRESHED 2016-10-29
RUN apt-get -y update && apt-get -y install ruby ruby-dev make nodejs
RUN gem install --no-rdoc --no-ri jekyll -v 2.5.3
VOLUME /data
VOLUME /var/www/html
WORKDIR /data
ENTRYPOINT ["jekyll", "build", "--destination=/var/www/html"]