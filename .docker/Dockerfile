FROM ruby:3.2.2-alpine

RUN apk update -qq && apk add gcompat libpq-dev nodejs vim g++ make

WORKDIR /workspace

ADD ../Gemfile /workspace/Gemfile
ADD ../Gemfile.lock /workspace/Gemfile.lock

RUN gem install bundler -v 2.4.19
RUN bundle install

CMD [ "rails", "s", "-b", "0.0.0.0" ]