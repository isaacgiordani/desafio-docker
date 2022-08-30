FROM node:14.15.4
LABEL maintainer="isaacgiordani@gmail.com"
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["npm", "start"]

# cd conversao-temperatura
# docker build -t isaacgiordani/conversao-temperatura:v1 .
# docker login
# docker push isaacgiordani/conversao-temperatura:v1
# docker tag isaacgiordani/conversao-temperatura:v1 isaacgiordani/conversao-temperatura:latest
# docker image ls
# docker push isaacgiordani/conversao-temperatura:latest
# docker-compose up -d
# http://localhost:8080/