Task:

As the system administrator of this organization, you are tasked with building a Docker image of a Django (Linux, nginx, Django, Postgres, Gunicorn) server, which could be made publicly available on Docker Hub, providing the candidate only with a link to the image and the installation command. All necessary services must be forwarded to the host via standard ports, HTTPS implementation is not required, the versions of Django, nginx and Postgres do not matter, as does the version of the Linux kernel. The project simply needs to have an admin panel working with a pre-defined login and password.

docker-compose -f docker-compose.prod.yml up -d --build

docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput

The admin panel is available at - http://localhost:1337/admin/

Login - admin,
Password - admin

Super admin management:

docker-compose -f docker-compose.prod.yml exec web python manage.py createsuperuser
