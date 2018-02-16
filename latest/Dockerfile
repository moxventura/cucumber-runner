FROM ruby:2.4.3-alpine3.7
MAINTAINER Jesper Jeeninga <jesper.jeeninga@trimm.nl>
RUN \
  apk update && \
  apk upgrade && \
  apk add build-base --no-cache && \
  gem install selenium-webdriver cucumber && \
  apk del build-base --purge && \
  rm -rf /var/cache/apk/*
