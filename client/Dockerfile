FROM node:18-alpine3.16

RUN npm install -g create-react-app

WORKDIR /app

COPY package*.json ./

RUN npm install -g npm@9.2.0

COPY package-lock*.json ./

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
