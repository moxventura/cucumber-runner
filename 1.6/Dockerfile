FROM ruby:2.5.1-alpine3.7
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
