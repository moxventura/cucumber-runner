FROM ruby:alpine
MAINTAINER Jesper Jeeninga <jesper.jeeninga@trimm.nl>
RUN \
  apk update && \
  apk upgrade && \
  apk add build-base --no-cache && \
  gem install selenium-webdriver cucumber gmail && \
  apk del build-base --purge && \
  rm -rf /var/cache/apk/*
