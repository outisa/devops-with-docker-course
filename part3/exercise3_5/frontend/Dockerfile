FROM node:alpine

WORKDIR /dist
COPY ./frontend-example/ .

RUN npm install && \
    npm run build && \
    npm install -g serve && \
    rm -rf /dist/node_modules/* && \
    adduser -D app

USER app

EXPOSE 5000

CMD serve -s -l 5000 dist
