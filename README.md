## Docker Django with MySQL5.7 and Nginx

## spec

- wsgi
  gunicorn
- webserver
  - nginx
- database
  - mysql5.7

## install

1. clone this repository
1. run `docker-compose up -d`
1. init database `docker-compose exec app python manage.py migrate`
1. collect static files `docker-compose exec app python manage.py collectstatic --noinput`
1. create super user `docker-compose exec app python manage.py createsuperuser`

## add your apps

`docker-compose exec app YOUR_COMMAND`

eg
`docker-compose exec app python manage.py startapp polls`

## restart your apps

`sh bin/restartapp.sh` or `docker-compose restart app`