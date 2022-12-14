FROM node:19-alpine3.15

WORKDIR /app

COPY package*.json ./

RUN npm install -g npm@9.2.0

COPY . .

CMD ["npm", "start"]



