# Разработка LMS-системы
_SPA (Single Page Application) веб-приложение_

Проект представляет собой разработку LMS-системы (Learning Management System), в которой пользователи могут размещать свои полезные материалы или курсы.
Результатом создания проекта будет бэкенд-сервер, который будет возвращать клиенту JSON-структуры.


## Предварительная настройка
 
используйте `.env.sample` для настройки параметров проекта в качестве примера и создайте `.env` с параметрами проекта.

## Настройки для развертывания и администрирования проекта с помощью Docker

* для создания образа используйте команду:
```bash
docker compose build
```

* для запуска проекта используйте команду:
```bash
docker compose up
```


* чтобы посмотреть статус проекта:
```bash
docker compose ps
```

* чтобы остановить проект используйте команду:
```bash
docker compose down
```

* чтобы посмотреть логи проекта:
```bash
docker compose logs
```

* попасть в базу данных PostgreSQL можно следующим образом:
```bash
docker compose exec {DB_HOST=из .env} psql -U {DB_USER=из .env} -d {DB_NAME=из .env}
```

* создать суперпользователя можно следующим образом:
```bash
docker compose exec app python manage.py createsuperuser
```

или

```bash
docker compose exec app python manage.py create_su
```