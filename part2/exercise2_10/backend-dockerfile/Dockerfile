FROM ubuntu:16.04

WORKDIR /dist
RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs 
COPY ./backend-example-docker .
RUN npm install

EXPOSE 8000
ENTRYPOINT npm start
