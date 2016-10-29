FROM ubuntu:latest
MAINTAINER Moon_Yue "luna825"
ENV REFRESHED_AT 2016-10-29
RUN apt-get -y update && apt-get -y install ruby ruby-dev build-essential redis-tools
RUN gem install --no-rdoc --no-ri sinatra json redis
RUN mkdir -p /opt/webapp
EXPOSE 4567
CMD ["/opt/webapp/bin/webapp"]