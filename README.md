<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <h1 align="center">Yii 2 Advanced Project Template</h1>
    <h2 align="center">Sistema de RH: Ache sua vaga!</h2>
    <br>
</p>

<p>
Neste projeto planejo criar um mvp de uma plataforma de vagas de RH, será possível logar como admin, recrutador e usuário. Cada um terá um nível de acesso diferente no sistema.
</p>

Para rodar as aplicações backend e frontend decidi que era necessário utilizar o docker que facilitaria o processo de configuração, o banco de dados escolhido foi o mysql.

Configure o arquivo `.env` com as credênciais de acesso:

```
DB_HOST=
DB_NAME=
DB_USER=
DB_PASSWORD=
APP_ENV=
APP_DEBUG=
```

Para subir os containers, digite no terminal:

`docker-compose up -d`

Acesse o container da aplicação:

`docker exec -it ache-sua-vaga-php-fpm-1 bash`

Rode a instalação de pacotes do composer:

`composer install`

Rode as migrations:

`php yii migrate`

Acesse a aplicação se tudo deu certo:

[Aplicação frontend:](http://frontend.test/)

[Aplicação backend:](http://backend.test/)

[PHPmyAdmin](http://localhost:8082/)

### Doc do framework

Yii 2 Advanced Project Template is a skeleton [Yii 2](https://www.yiiframework.com/) application best for
developing complex Web applications with multiple tiers.

The template includes three tiers: front end, back end, and console, each of which
is a separate Yii application.

The template is designed to work in a team development environment. It supports
deploying the application in different environments.

Documentation is at [docs/guide/README.md](docs/guide/README.md).

[![Latest Stable Version](https://img.shields.io/packagist/v/yiisoft/yii2-app-advanced.svg)](https://packagist.org/packages/yiisoft/yii2-app-advanced)
[![Total Downloads](https://img.shields.io/packagist/dt/yiisoft/yii2-app-advanced.svg)](https://packagist.org/packages/yiisoft/yii2-app-advanced)
[![build](https://github.com/yiisoft/yii2-app-advanced/workflows/build/badge.svg)](https://github.com/yiisoft/yii2-app-advanced/actions?query=workflow%3Abuild)

## DIRECTORY STRUCTURE

```
common
    config/              contains shared configurations
    mail/                contains view files for e-mails
    models/              contains model classes used in both backend and frontend
    tests/               contains tests for common classes
console
    config/              contains console configurations
    controllers/         contains console controllers (commands)
    migrations/          contains database migrations
    models/              contains console-specific model classes
    runtime/             contains files generated during runtime
backend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains backend configurations
    controllers/         contains Web controller classes
    models/              contains backend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for backend application
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
frontend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains frontend configurations
    controllers/         contains Web controller classes
    models/              contains frontend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for frontend application
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
    widgets/             contains frontend widgets
vendor/                  contains dependent 3rd-party packages
environments/            contains environment-based overrides
```
