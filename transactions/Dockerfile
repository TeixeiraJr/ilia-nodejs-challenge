FROM node:alpine

WORKDIR /usr/app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build
COPY .env ./dist/
WORKDIR /usr/app/dist

EXPOSE 3001

CMD node index.js