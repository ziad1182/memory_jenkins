FROM node:14.16.1

WORKDIR /index

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5000

CMD ["node","index.js"]