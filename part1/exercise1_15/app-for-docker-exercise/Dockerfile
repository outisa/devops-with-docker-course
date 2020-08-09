FROM node:13.12.0

WORKDIR /app
ENV PATH /app/node_modules/.bin:$PATH
COPY package.json ./
COPY package-lock.json ./
COPY  . ./

RUN npm install
RUN npm run build
RUN npm install -g serve
EXPOSE 5000
CMD serve -s build
