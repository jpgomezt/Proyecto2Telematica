#React build
FROM node:14.19.1-alpine3.14 as react-build

WORKDIR /usr/src/frontend

COPY . .

RUN npm install

RUN npm run build
 
#Nginx setup
FROM nginx:1.12.0

RUN rm -f /etc/nginx/nginx.conf

COPY ./nginx.conf /etc/nginx/nginx.conf

COPY --from=react-build /usr/src/frontend/build /usr/share/nginx/html/bookstore