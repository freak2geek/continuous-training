FROM ubuntu:16.04

RUN apt-get update
RUN apt-get -y install apache2
RUN apt-get -y install wget
RUN apt-get -y install unzip
EXPOSE 81
CMD /usr/sbin/apache2ctl -D FOREGROUND
