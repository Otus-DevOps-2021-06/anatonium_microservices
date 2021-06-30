FROM ruby:2.2
RUN apt-get update && apt-get install -y ruby-full=1:2.3.0+1 ruby-dev=1:2.3.0+1 uild-essential=12.1ubuntu2 --no-install-recommends && gem install bundler --no-ri --no-rdoc

ENV APP_HOME /app
WORKDIR $APP_HOME
COPY . $APP_HOME
RUN bundle install

ENV POST_SERVICE_HOST post
ENV POST_SERVICE_PORT 5000
ENV COMMENT_SERVICE_HOST comment
ENV COMMENT_SERVICE_PORT 9292

CMD ["puma"]
