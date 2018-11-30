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
