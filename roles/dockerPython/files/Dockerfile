# file: files/Dockerfile

#FROM python:3.6.1-alpine
#FROM python:3.7.0b4-alpine3.7

FROM resin/raspberry-pi-alpine-python:latest

RUN apk update \
  && apk add \
    build-base \

RUN mkdir /usr/src/app
WORKDIR /usr/src/app

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
