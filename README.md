# Exemplo do uso do Docker Compose com NginX/GoLang/MySQL

Repositório criado a partir de um Fork do repósitorio do Docker ([awesome-compose](https://github.com/docker/awesome-compose)), dando destaque ao exemplo do Docker Compose com uma aplicação em NginX, GoLang e MySQL.

> ReadME inspirado no mesmo repositório e projeto do awesome-compose

## Setup do Projeto

Primeiro confira que o Docker e o Docker Compose estão instalados:

-   Windows/macOS:
    [Docker Desktop](https://www.docker.com/get-started) (Importante que tenha o WSL2 instalado)

Depois, entre na pasta com o projeto (nginx-golang-mysql), lá você irá localizar o arquivo `compose.yaml`,
esse que contém as configurações necessárias para os containers e a aplicação em sí para assim executar o Docker Compose.
Asegurando que está na pasta correta, execute a seguinte linha de comando para subir a aplicação:

```console
docker compose up -d
```

Caso queira parar ela execute:

```console
docker compose down
```

## 🏆 Resultado esperado

Quando a aplicação for levantada, isso ocorrerá na porta 80.

Lista de containers que deverão estar disponíveis e ligados:

```console
$ docker compose ps
NAME                           COMMAND                  SERVICE             STATUS              PORTS
nginx-golang-mysql-backend-1   "/code/bin/backend"      backend             running
nginx-golang-mysql-db-1        "docker-entrypoint.s…"   db                  running (healthy)   3306/tcp
nginx-golang-mysql-proxy-1     "/docker-entrypoint.…"   proxy               running             0.0.0.0:80->80/tcp
l_db_1
```

Acesse `http://localhost:80` para ver o resultado e a página web.


## 👥 Integrantes do Grupo

-   **_Arthur Fagundes Oliveira_**
-   **_Bruno Cenci Basso_**
-   **_Gabriel Soldatelli_**
-   **_Guilherme Garcia Guedes_**

## Créditos
-  [Docker](https://github.com/docker/awesome-compose)
