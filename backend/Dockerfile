FROM python:3.8-slim

WORKDIR /foodgram

COPY requirements.txt .
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip3 install -r requirements.txt --no-cache-dir

COPY . .

CMD gunicorn app.wsgi:application --bind 0.0.0.0:8000
