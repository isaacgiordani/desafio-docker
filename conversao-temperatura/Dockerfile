FROM node:14.15.4
LABEL maintainer="isaacgiordani@gmail.com"
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["npm", "start"]

# docker build -t isaacgiordani/conversao-temperatura:v1 .
# docker login
# docker push isaacgiordani/conversao-temperatura:v1
# docker tag isaacgiordani/conversao-temperatura:v1 isaacgiordani/conversao-temperatura:latest
# docker image ls
# docker push isaacgiordani/conversao-temperatura:latest
# docker container run -d -u 1000 -p 8080:8080 --cpus="0.5" isaacgiordani/conversao-temperatura:v1