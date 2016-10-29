FROM ubuntu:latest
MAINTAINER Moon_Yue "luna825@qq.com"
ENV REFRESHED_AT 2016-10-29
RUN apt-get -yqq update && apt-get -y install redis-server redis-tools 
EXPOSE 6379
ENTRYPOINT ["/usr/bin/redis-server"]
CMD []