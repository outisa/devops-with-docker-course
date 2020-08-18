FROM ubuntu:16.04

WORKDIR /dist
COPY ./backend-example .

RUN apt-get update && apt-get install -y curl \
    && curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs \
    && npm install \
    && apt-get purge -y --auto-remove curl \
    && rm -rf /var/lib/apt/lists/*

COPY ./logs.txt .

EXPOSE 8000
CMD npm start
