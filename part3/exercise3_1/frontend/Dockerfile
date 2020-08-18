FROM ubuntu:16.04

WORKDIR /dist
COPY ./frontend-example/ .

RUN apt-get update && apt-get install -y curl \
    && curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs \
    && npm install \
    && npm run build \
    && npm install -g serve \
    && apt-get purge -y --auto-remove curl \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /dist/node_modules/* 

EXPOSE 5000

CMD serve -s -l 5000 dist
