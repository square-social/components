# Components
This repository contains the definitions of general components needed for development of the Square system.

The main development dependencies are managed through Docker via a `docker-compose.yml` file.

To start up the dependencies:
```shell
docker-compose up
```
> All components store data in a `./app-volume` directory, relative to the compose file. If this doesn't exist yet, you might need to create it, and grant permissions via `chmod -R 777 app-volume` to allow docker to use it.

