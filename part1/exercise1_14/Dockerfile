FROM ruby:2.6.0

WORKDIR /mydir
COPY ./rails-example-project .
RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs 
RUN bundle install
RUN rails db:migrate
EXPOSE 3000
CMD rails s
