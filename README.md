# Desafio Docker Devops Pro

## Pré requisitos
- Ter o docker e docker-compose instalados.
- Não ter nenhum outro serviço rodando nas portas utilizadas.


## Mongo + Mongo-Express
1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample.

2 - Executar o comando para subir os containers

```
cd mongo
docker-compose up -d
```

3 - Acessar a URI no browser http://localhost:8081/

4 - Para desprovisionar

```
cd mongo
docker-compose down
```

## MariaDB + PhpMyAdmin
1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample

2 - Executar o comando para subir os containers

```
cd mariadb
docker-compose up -d
```

3 - Acessar a URI no browser http://localhost:8082/

4 - Para acessar

Servidor: mariadb
Utilizador: root
Palavra Passe: examplepassroot

5 - Para desprovisionar

```
cd mariadb
docker-compose down
```

## PostgreSQL + PgAdmin
1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample

2 - Executar o comando para subir os containers

```
cd postgres
docker-compose up -d
```

3 - Acessar a URI no browser http://localhost:8083

4 - Informar o e-mail e senha passados através do arquivo .env

5 - Botão direito em Servers >> Register >> Server...

    Aba General
        Name: postgres
    Aba Connection
        Host: postgres
        Port: 5432
        Username: postgres

6 - Para desprovisionar

```
cd postgres
docker-compose down
```

## Redis + Redis Commander
1 - Executar o comando para subir os containers

```
cd redis
docker-compose up -d
```

2 - Acessar a URI no browser http://localhost:8084

## Wordpress
1 - Executar o comando para subir os containers

```
cd wordpress
docker-compose up -d
```

2 - Acessar a URI no browser http://localhost:8080

## Conversao-temperatura (Aplicação escrita em NodeJS)
Comandos utilizados para construir a imagem:

```
cd conversao-temperatura
docker build -t isaacgiordani/conversao-temperatura:v1 .
docker login
docker push isaacgiordani/conversao-temperatura:v1
docker tag isaacgiordani/conversao-temperatura:v1 isaacgiordani/conversao-temperatura:latest
docker image ls
docker push isaacgiordani/conversao-temperatura:latest
docker-compose up -d
http://localhost:8080/
```
## Conversao-distancia (Aplicação escrita em Python utilizando Flask Aplicação escrita em C# utilizando)
Comandos utilizados para construir a imagem:

```
cd conversao-distancia
docker build -t isaacgiordani/conversao-distancia:v1 .
docker login
docker push isaacgiordani/conversao-distancia:v1
docker tag isaacgiordani/conversao-distancia:v1 isaacgiordani/conversao-distancia:latest
docker image ls
docker push isaacgiordani/conversao-distancia:latest
docker-compose up -d
http://localhost:8090/
```

## Conversao-peso (ASP.NET Core)
Comandos utilizados para construir a imagem:

```
cd conversao-peso/src/
docker build -t isaacgiordani/conversao-peso:v1 .
docker login
docker push isaacgiordani/conversao-peso:v1
docker tag isaacgiordani/conversao-peso:v1 isaacgiordani/conversao-peso:latest
docker image ls
docker push isaacgiordani/conversao-peso:latest
cd conversao-peso/
docker-compose up -d
http://localhost:8000/
```

## Rotten-Potatoes

1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample

2 - Executar o comando para subir os containers

```
cd rotten-potatoes/src/
docker-compose up -d
```

Comandos utilizados para construir a imagem:

```
cd rotten-potatoes/src/
docker build -t isaacgiordani/rotten-potatoes:v1 .
docker login
docker push isaacgiordani/rotten-potatoes:v1
docker tag isaacgiordani/rotten-potatoes:v1 isaacgiordani/rotten-potatoes:latest
docker image ls
docker push isaacgiordani/rotten-potatoes:latest
docker-compose up -d
http://localhost:5000/
```

## Kube-news
1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample

2 - Executar o comando para subir os containers

```
cd kube-news/src/
docker-compose up -d
```

Comandos utilizados para construir a imagem:

```
cd kube-news/src
docker build -t isaacgiordani/kube-news:v1 .
docker login
docker push isaacgiordani/kube-news:v1
docker tag isaacgiordani/kube-news:v1 isaacgiordani/kube-news:latest
docker image ls
docker push isaacgiordani/kube-news:latest
docker-compose up -d
http://localhost:8080/
```

## Desprovisionando todo o ambiente
CUIDADO AO EXECUTAR O COMANDO, POIS EXCLUIRÁ TODOS OS CONTAINERS, IMAGENS, REDES E *VOLUMES*.

```
sudo sh docker-clear.sh
```