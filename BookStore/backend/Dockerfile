FROM node:14.19.1-alpine3.14

WORKDIR /usr/src/backend

COPY . .

RUN npm install

EXPOSE 5000

CMD ["node", "server.js"]

