# Docker (Django + Gunicorn + NginX + PostgreSQL)
<hr>

> **Warning**
> В данном проекте все пароли и ключи прописаны в коде. Пожалуйста, скрывайте эти данные



### [ссылка на образ](https://hub.docker.com/repository/docker/ddakhmetov/django_for_server)
Если ссылка не работает, можно скопировать путь до образа:

https://hub.docker.com/repository/docker/ddakhmetov/django_for_server

## Скачать образ можно командой:
````shell
docker pull ddakhmetov/django_for_server
````

## Запускается командой:
```shell
docker run -p 8000:8000 -p 80:80 ddakhmetov/django_for_server
```

## Административный web-сайт:
### Для входа используйте следующие данные:
**Логин:** admin

**Пароль:** admin

<hr>

## Сборка образа:
#### Для сборки образа необходимо сделать следующее:
1. Скачайте этот проект. Например: `git pull https://github.com/denisakhmetovdev/docfile.git`
2. В терминале перейдите в директорию, где находится Dockerfile этого проекта
3. Выполните следующую команду
```shell
docker build -t <имя_будущего_образа> .
```
Например:
```shell
docker build -t e4 .
```

Теперь можно залить образ на Docker Hub

## Заливаем образ на Docker Hub
1. Выполните действия, описанные ниже:
```shell
# Логин на Docker Hub
docker login

# Тэгируем образ перед публикацией
docker tag django_for_server ddakhmetov/django_for_server:latest

# Публикуем образ на Docker Hub
docker push <ваш_username_на_docker-hub>/<имя_образа>:latest
```

Например:
```shell
docker tag django_for_server ddakhmetov/django_for_server:latest
```
```shell
docker push ddakhmetov/django_for_server:latest
```
