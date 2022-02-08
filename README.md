# Conversao Temperatura


FROM node:14.17.5
WORKDIR /app
COPY package*.json /app/
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]




docker image build -t teclinux/conversao-temperatura:v1 .

docker container run -d -p 8080:8080 teclinux/conversao-temperatura:v1