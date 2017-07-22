FROM python:3

WORKDIR /usr/src/app

COPY src/requirements.txt .
RUN pip install -r requirements.txt
RUN pip install uwsgi

COPY src/ .

RUN bash -c "python manage.py migrate"

COPY uwsgi.ini .
CMD ["uwsgi", "--ini", "uwsgi.ini"]