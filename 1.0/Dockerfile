FROM ruby:2.4.3-alpine
MAINTAINER Jesper Jeeninga <jesper.jeeninga@trimm.nl>
RUN \
  apk update && \
  apk upgrade && \
  apk add build-base --no-cache && \
  gem install selenium-webdriver -v 3.9.0 && \
  gem install cucumber -v 3.1.0 && \
  apk del build-base --purge && \
  rm -rf /var/cache/apk/*
