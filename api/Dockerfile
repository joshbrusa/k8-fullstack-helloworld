FROM node as build
WORKDIR /code
COPY package*.json .
RUN npm install
COPY . .
RUN npm run build

CMD [ "npm", "start"]