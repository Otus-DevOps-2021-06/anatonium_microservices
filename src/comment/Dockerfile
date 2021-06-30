FROM ruby:2.2
RUN apt-get update -qq && apt-get install -y build-essential

WORKDIR /app
COPY . /app
RUN bundle install

ENV COMMENT_DATABASE_HOST comment_db
ENV COMMENT_DATABASE comments

CMD ["puma"]
