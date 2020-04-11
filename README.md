<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

## Laravel CRUD Docker

- Laravel 7.0
- Vue.js
- Database (Sqlite, MariaDB, Mongo, etc...)
- Docker

<br>

### Install

```
git clone https://github.com/andreustimm/laravel-crud-docker.git
cd laradock
git submodule update
cp env-example .env
```

<br>

### Laradock's Configuration

To edit `.env` with your preference

**Example:**

```
APP_CODE_PATH_HOST=../web/
PHP_VERSION=7.3
```

**MariaDB**

```
MARIADB_VERSION=latest
MARIADB_DATABASE=laravel
MARIADB_USER=root
MARIADB_PASSWORD=root
MARIADB_PORT=3306
MARIADB_ROOT_PASSWORD=root
```

**Nginx**

```
NGINX_HOST_HTTP_PORT=9090
NGINX_HOST_HTTPS_PORT=443
...
NGINX_PHP_UPSTREAM_PORT=9000
NGINX_SSL_PATH=./nginx/ssl/
```

### Project's Configuration
```
cd web
composer install
npm run prod
php artisan migrate
php artisan passport:install
```

<br>

### Run Project

To run the `docker-compose up -d` with your favorite stack.

**Example:** For run `nginx`, `apache`, `mariadb`, `mongo`, `redis`

- [Documentation](https://laradock.io/)
- [Github Laradock](https://github.com/laradock/laradock)

```
cd laradock
sudo docker-compose up -d nginx
```

<br>

### Roadmap

- Release Version 0.1 - Install Laravel and start project
- Release Version 0.2 - CRUD Frontend Vue
- Release Version 0.3 - Docker's Implanting
- Release Version 0.4 - Documentation
- Release Version 0.5 - API CRUD
- Release Version 0.7 - Auth API *come soon*
- Release Version 0.8 - TDD *come soon*

<br>

### Author

- [Portfolio](https://www.zorbit.com.br/portfolio)
- [Linkedin](https://www.linkedin.com/in/andreus-timm-2490b134/)

### License

[MIT license](https://opensource.org/licenses/MIT).
