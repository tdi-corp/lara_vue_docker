# Laravel 11 & Vue 3 SPA Starter Kit
[![](https://img.shields.io/badge/Vue-v3.4-04C690?style=flat)](https://vuejs.org/)
[![](https://img.shields.io/badge/Laravel-v11-ff2e21?style=flat)](https://laravel.com)

## Technology
- PHP-FPM 8.3
- Laravel 11
- Node 20.16
- Vue, Vuex
- Docker & Docker Compose
- Nginx
- Mysql

## How it works
### Containers
1) **api**: serves the backend app (laravel app)
2) **client**: serves the fronted app (vue app)
3) **webserver**: services static content, storage, and passes traffic to api & client containers (proxy)
4) **mysql**: main database connection

## Installation
### Development Environment
it includes compiling and hot-reloading for development
```
cp api/.env.dev.example api/.env.dev

// then =>

docker-compose -f docker-compose.yml -f docker-compose.dev.yml up --build

// then =>

// run the migrations
docker exec -it spa-dev-api-1 php artisan migrate --seed
```
- To access the api open http://localhost:8000
- To access the client open http://localhost:3000

