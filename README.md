Задача:

    Как системному администратору данной организации вам поставлена задача собрать на докер образ Django (Linux, nginx, Django, Postgres, Gunicorn) сервера, который можно было бы выложить в публичный доступ на Docker Hub, предоставляя кандидату только ссылку на образ и команду для установки. Все нужные сервисы должны быть проброшены на хост по стандартным портам, реализация HTTPS не требуется, версии Django, nginx и Postgres не имеют значения, как и версия ядра Linux. В проекте просто должна работать админка с заранее прописанным логином и паролем.

docker-compose -f docker-compose.prod.yml up -d --build

docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput

Админка доступна по адресу - http://localhost:1337/admin/ 

Login - admin,
Password - admin

Управление супер админом:

docker-compose -f docker-compose.prod.yml exec web python manage.py createsuperuser
