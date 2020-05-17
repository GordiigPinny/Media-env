# meetuper-env
Docker Compose MediaService

## Зависимости
Для запуска необходимо наличие [Docker](https://www.docker.com/)

## Запуск

### 1. Собрать локально контейнер бекэнда
```
$ cd django
$ docker build -f Dockerfile -t tech_rost_python:latest .
```

### 2. Создать `.env` файл, скопировав `.env.example` и заполнить все константы
* `BACKEND_PATH` - путь к репозиторию бекэнда (master git-ветка)
* `DJANGO_APPNAME` -  имя модуля Django с настройками (MediaService)
* `WSGI_WORKERS` - количество воркеров gunicorn для django


### 3. Запуск
```
$ docker-compose up
```

