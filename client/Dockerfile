FROM node:18-alpine3.16


WORKDIR /app

COPY package*.json ./

RUN npm install -g npm@9.2.0

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
