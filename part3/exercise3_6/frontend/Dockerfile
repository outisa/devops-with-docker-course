FROM node:alpine as builder

WORKDIR /dist
COPY ./frontend-example/ .

RUN npm install && \
    npm run build && \
    rm -rf /dist/node_modules/*

FROM node:alpine as app

COPY --from=builder dist .
RUN npm install -g serve && \
    adduser -D app

USER app

EXPOSE 5000

CMD serve -s -l 5000 dist
