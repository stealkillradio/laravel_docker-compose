# Docker for appwilio.ru

Конфигурация контейнеров запуска сайта appwilio.ru

## Зупуск контейнеров

```
docker-compose build
```
```
docker-compose up
```
* Установить зависимости:

```
docker exec -ti php-fpm-appwillio.ru composer install
```
* Сделать папку storage доступной:

```
chmod -R 777 public/storage
chmod -R 777 public/bootstrap
```

* Сайт будет доступен по адресу localhost:8088
* База данных по умолчанию name: appwilio.ru pass: test

