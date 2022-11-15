# Components
This repository contains the definitions of general components needed for development of the Square system.

The main development dependencies are managed through Docker via a `docker-compose.yml` file.

To start up the dependencies:
```shell
docker-compose up
```
> All components store data in a `./app-volume` directory, relative to the compose file. If this doesn't exist yet, you might need to create it, and grant permissions via `chmod -R 777 app-volume` to allow docker to use it.

### Postgres & Adminer
Some services require the use of a relational, consistent data store, and for that we use Postgres. You can use Adminer at http://localhost:8080/ to browse the database. Connect with the following credentials:
```properties
System   = PostgreSQL
Server   = postgres:5432
Username = postgres-dev
Password = postgres-dev-pass
Database = postgres-dev
```