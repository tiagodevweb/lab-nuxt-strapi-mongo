## Lab Nuxt, Strapi and Mongo

#### Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Install

```bash
$ docker-compose up -d --build
```
#### Monitor installation process
```bash
$ docker-compose logs --tail=all -f | grep strapi
$ docker-compose logs --tail=all -f | grep nuxt
```

#### Optional in .env
It is necessary to go up the containers again after changing the variables above.
```php
# Docker variables
DATABASE_CLIENT=mongo
DATABASE_NAME=strapi
DATABASE_HOST=mongodb
DATABASE_PORT=27017
DATABASE_USERNAME=strapi
DATABASE_PASSWORD=password
MONGO_INITDB_ROOT_USERNAME=strapi
MONGO_INITDB_ROOT_PASSWORD=password
HOST=0.0.0.0
PORT=1337
```