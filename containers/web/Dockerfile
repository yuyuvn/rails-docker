FROM ruby:2.3.3
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /app
WORKDIR /tmp
COPY ./app/Gemfile Gemfile
COPY ./app/Gemfile.lock Gemfile.lock
RUN bundle install
ADD . /app
WORKDIR /app
