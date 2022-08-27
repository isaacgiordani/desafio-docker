# Desafio Docker Devops Pro

## Observações
- O bind das portas é proposital permitindo o uso de ferramentas instaladas localmente, não se limitando ao uso da ferramenta criada no container.
- O mapeamento dos volumes também é proposital para persistir os dados e facilitar o backup.

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

4 - Para desprovisionar

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

## Wordpress

## 

## Desprovisionar todo o ambiente
CUIDADO AO EXECUTAR O COMANDO, POIS EXCLUIRÁ TODAS OS CONTAINERS, IMAGENS, REDES E *VOLUMES*.

```
sudo sh docker-clear.sh
```