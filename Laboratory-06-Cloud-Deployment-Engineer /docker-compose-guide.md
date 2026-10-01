# Docker Compose Guide

## Docker Compose File

The `docker-compose.yml` file serves as the configuration or blueprint for running the Nextcloud application and MariaDB database together.

```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## The `services:` Block

The `services:` section contains the different containers required by the application. For this project, it includes two services: `database`, which runs MariaDB, and `app`, which runs Nextcloud.

The MariaDB service handles the database, while the Nextcloud service runs the web application that users access.

## How Nextcloud Finds the Database

Nextcloud uses the following environment variable to identify the database service:

```yaml
- MYSQL_HOST=database
```

The word `database` refers to the MariaDB service name defined in the Compose file. Docker Compose places the services on the same network, allowing Nextcloud to connect to MariaDB by using its service name instead of an IP address.

## Difference between `docker run` and `docker-compose up -d`

The `docker run` command is commonly used when creating and starting an individual Docker container. I used this method in earlier activities for containers such as Nginx and MinIO.

On the other hand, `docker-compose up -d` is useful when an application requires multiple connected containers. The configuration for all the services is written in the YAML file, and Docker Compose can then create and start the entire application stack using one command.
