FROM ruby:2.3.0
RUN apt-get update && apt-get install -y build-essential \
                                         nodejs
RUN mkdir /docker-test
WORKDIR /docker-test
ADD Gemfile /docker-test/Gemfile
ADD Gemfile.lock /docker-test/Gemfile.lock
RUN bundle install
ADD hello-world.rb /docker-test/hello-world.rb

EXPOSE 4567

ENTRYPOINT [ "ruby", "/docker-test/hello-world.rb" ]