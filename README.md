# README

# Docker Network
docker network create everything_app

# NGINX+LetsEncrypt
```shell
docker-compose build
docker-compose up -d

docker-compose stop
docker-compose start
```

# Rails
```shell
docker build -t app ./rails/.
docker volume create app-storage
docker run -d --rm -it --name rails --env-file ./rails/.env -v app-storage:/rails/storage --network everything_app app
```

# Vue
```shell
docker build -t secondary secondary/.
docker run -d --name vite --env ./secondary/.env --network everything_app secondary

```
# Postgres
```shell
mkdir psql/postgres-data
docker build -t psql ./psql/.
docker run -d --name postgres --env-file ./psql/.env -v postgres-data:/var/lib/postgresql/data --network everything_app psql