FROM python:3.7-alpine
ENV PYTHONUNBUFFERED 1
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
RUN apk update \
  && apk add --virtual build-tools gcc python3-dev musl-dev \
  && apk add mariadb-dev
ADD . /usr/src/app/
RUN pip install -r requirements.txt
RUN apk del build-tools
