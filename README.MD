# Docker for laravel

Конфигурация контейнеров запуска сайта на Laravel

Перед запуском необходимо склонировать код проекта в каталог public

* Сделать папку storage доступной:

```
chmod -R 777 public/storage
chmod -R 777 public/bootstrap
```
## Зупуск контейнеров

```
docker-compose build
```
```
docker-compose up
```
* Установить зависимости:

```
docker exec -ti php-fpm composer install
```
* Сайт будет доступен по адресу localhost:8088
* База данных по умолчанию db_name: homestead user: root pass: secret

