FROM node:22

WORKDIR /app

EXPOSE 3000

COPY package.json package-lock.json ./

ENV HTTPS=true
ENV SSL_CRT_FILE=/app/certs/selfsigned.crt
ENV SSL_KEY_FILE=/app/certs/selfsigned.key

RUN npm install

COPY . .

CMD ["npm", "start"]




