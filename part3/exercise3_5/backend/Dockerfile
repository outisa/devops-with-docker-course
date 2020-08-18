FROM node:alpine

WORKDIR /dist
COPY ./backend-example .
COPY ./logs.txt .

RUN npm install && \
    adduser -D app && \
    chown -R app: /dist/

USER app 
EXPOSE 8000
CMD ["node","index.js"]
