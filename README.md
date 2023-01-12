# README

# NGINX+LetsEncrypt
```shell
docker-compose build
docker-compose up -d

docker-compose stop
docker-compose start
```

# Rails
```shell
docker build -t app .
docker volume create app-storage
docker run -d --rm -it --env-file .env -v app-storage:/rails/storage --network demo_default app
```

# Vue
```shell
docker build -t secondary secondary/.
docker run -d --network demo_default secondary

```
# Postgres
```shell
cd psql
docker build -t psql ./psql/.
docker run -d --name postgres --env-file ./psql/.env -v postgres-data:/var/lib/postgresql/data --network demo_default psql