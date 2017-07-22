FROM python:3

WORKDIR /usr/src/app

COPY src/requirements.txt .
RUN pip install -r requirements.txt

COPY src/ .

ENV DEBUG=False

CMD ["celery", "-A", "core.celery:app", "worker", "--loglevel=info"]