FROM python:3

WORKDIR /usr/src/app

COPY src/requirements.txt .
RUN pip install -r requirements.txt
RUN pip install uwsgi

COPY src/ .
COPY uwsgi.ini .

ENV DEBUG=0