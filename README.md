# API server platform comparison research project

This repository is a part of **"Performance comparison of development frameworks in selected environments in REST API architecture"** research project.

## Description

The purpose of the aforementioned paper is to compare the performance of development frameworks in selected environments in the REST API architecture. The comparative analysis was carried out based on five applications that were implemented based on the common [OpenAPI specification](openapi.yaml).

The Laravel, ASP.NET, Django REST Framework, Express.js and Spring Boot development platforms have been selected as test subjects. All applications were connected to the same [MySQL database](database/db.sql). 

List of applications implemented as a part of the project:
- [Laravel API server](https://github.com/MAtt5816/laravel-api-server) 
- [ASP.NET API server](https://github.com/MAtt5816/aspNet-api-server) 
- [Django REST Framework API server](https://github.com/MAtt5816/django-api-server) 
- [Express.js API server](https://github.com/MAtt5816/expressJS-api-server) 
- [Spring Boot API server](https://github.com/MAtt5816/spring-api-server) 

## Getting Started

### Dependencies

* Frameworks:
  * [Laravel v.11.9](https://github.com/laravel/laravel/tree/11.x)
  * [ASP.NET v.8.0](https://github.com/dotnet/aspnetcore/tree/v8.0.6)
  * [Django REST Framework v.3.15.2](https://github.com/encode/django-rest-framework/tree/3.15.2)
  * [Express.js v.4.19.2](https://github.com/expressjs/express/tree/4.19.2)
  * [Spring Boot v.3.3.2](https://github.com/spring-projects/spring-boot/tree/v3.3.2)
* Database:
  * [MySQL v.9.0](https://hub.docker.com/_/mysql)

### Installing & running

1. Prepare `.env` file:
    ```shell
    cp .env.example .env
    ```
2. Fill environmental variables in `.env` file.
3. Using docker-compose:
    ```shell
    # one of below command
    docker compose -f laravel-api-server.prod.docker-compose.yml up -d
    docker compose -f aspnet-api-server.prod-azure.docker-compose.yml up -d
    docker compose -f django-api-server.prod.docker-compose.yml up -d
    docker compose -f express-api-server.prod.docker-compose.yml up -d
    docker compose -f spring-api-server.prod.docker-compose.yml up -d
    ```

> **Note:** Database is running in violate mode, i.e. it will be reset to the default dataset after restart.

> **Note:** If you would like to run docker-compose with non-violate database, use `*.dev.docker-compose.yml` instead `*.prod.docker-compose.yml`.

### Stopping or resetting dataset
```shell
docker-compose -f docker-compose.prod.yml down -v
```

## Database structure

![student_data DB schema.png](database/student_data%20DB%20schema.png)

## Author

Mateusz Szewczyk

@[GitHub](https://github.com/MAtt5816)
