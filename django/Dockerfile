FROM python:3.7-alpine3.10
ENV PYTHONUNBUFFERED 1

RUN apk add --update \ 
    bash \
    build-base \
    linux-headers \
    libc6-compat \
    python3-dev \
    git \
    gcc \
    python-dev \
    libffi-dev \
    postgresql-dev \
    jpeg-dev \
    zlib-dev \
    unixodbc-dev && rm -rf /var/cache/apk/*

RUN mkdir /code
WORKDIR /code

ADD requirements.txt /code/
RUN pip install -r requirements.txt
