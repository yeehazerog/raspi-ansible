# file: files/Dockerfile

FROM resin/raspberry-pi-alpine-python:latest

MAINTAINER yeeha zeroG <yeeha.zeroG@gmail.com>

RUN apk update

WORKDIR home/pi/storage/docker/applications/telegram

RUN python setup.py install

#
#
# This part install telegram
#RUN apk add \
#  libreadline-dev \
#  libconfig-dev \
#  libssl-dev \
#  lua5.2 \
#  liblua5.2-dev \
#  libevent0dev \
#  make
