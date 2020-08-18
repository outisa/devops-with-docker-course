FROM ubuntu:16.04

WORKDIR /dist
COPY ./backend-example .
COPY ./logs.txt .
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    npm install && \
    useradd -m app && \
    chown -R app: /dist/

USER app 
EXPOSE 8000
CMD ["npm","start"]
