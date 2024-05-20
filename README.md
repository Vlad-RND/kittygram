<!-- [![Main Kittygram workflow](https://github.com/Vlad-RND/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/Vlad-RND/kittygram_final/actions/workflows/main.yml) -->

# Kittygram
### Описание проекта:
Проект kittygram представляет собой сайт, где пользователь может размещать фотографии 
своих котиков, предварительно зарегистрировавшись. К фотографиям необходимо добавить имя, 
выбрать окрас (из имеющегося списка) и поделиться достижениями своего любимца - выбрать их из списка или добавить новые.
Пользователь может редактировать/удалять свои записи и только просматривать чужие.

### Используемые библиотеки:
python-dotenv 1.0.1, Django 3.2.3, djangorestframework 3.12.4, django-cors-headers 3.13.0,
djoser 2.1.0, webcolors 1.11.1, psycopg2-binary 2.9.3, Pillow 9.0.0, pytest 6.2.4,
pytest-django 4.4.0, pytest-pythonpath 0.7.3, PyYAML 6.0, gunicorn 20.1.0

### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/Vlad-RND/kittygram.git
```
```
cd kittygram
```

### Создать в директории проекта и заполнить .env:
Пример заполнения файла содержится в .env.example

### Подтянуть последнюю версию проекта:
```
docker compose -f docker-compose.production.yml pull
```

### Запустить инструкцию с автоматическим запуском контейнеров проекта:
```
docker compose -f docker-compose.production.yml up
```

### Создать миграции в БД проекта:
```
docker compose -f docker-compose.production.yml exec backend python manage.py migrate
```

### Собрать статику бекэнда и скопировать в нужную директорию:
```
docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
```
```
docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```

### Функционал:
- Регистрация;
- Добавление питомца с фотографией и "достижениями";
- Добавление "достижений"

Автор - Vlad-RND, GIT - https://github.com/Vlad-RND
