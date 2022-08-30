FROM node:16.15.0
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]

# cd kube-news/src
# docker build -t isaacgiordani/kube-news:v1 .
# docker login
# docker push isaacgiordani/kube-news:v1
# docker tag isaacgiordani/kube-news:v1 isaacgiordani/kube-news:latest
# docker image ls
# docker push isaacgiordani/kube-news:latest
# docker-compose up -d
# http://localhost:8080/