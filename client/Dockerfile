# Stage 1
FROM node:16.14.2-alpine as node

WORKDIR /app 

COPY package*.json /app/

RUN npm i npm@latest -g

RUN npm install

COPY ./ /app/

RUN npm run build

#stage 2
FROM nginx:1.15
COPY --from=node /app/build/ /usr/share/nginx/html
COPY ./nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80