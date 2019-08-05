FROM ruby:2.6.3-alpine3.10
MAINTAINER Jesper Jeeninga <jesper.jeeninga@trimm.nl>
COPY ./Gemfile /Gemfile
COPY ./Gemfile.lock /Gemfile.lock
RUN \
  apk update && \
  apk upgrade && \
  apk add build-base bash --no-cache && \
  gem install bundler && \
  bundle install && \
  rm -rf /Gemfile* && \
  apk del build-base --purge && \
  rm -rf /var/cache/apk/*
ENTRYPOINT ["bash", "-c"]
