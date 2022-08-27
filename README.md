# Desafio Docker Devops Pro

## MONGO
1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample.

2 - Executar o comando para subir os containers

```
cd mongo
docker-compose up -d
```

## MariaDB
1 - Criar o arquivo .env com usuário e senha desejada com base no arquivo envsample
2 - Executar o comando para subir os containers

```
cd mariadb
docker-compose up -d
```

## PostgreSQL
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