FROM python:3.11-slim

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app/files/

COPY /requirements.txt /app/files/requirements.txt

RUN pip install --upgrade pip
RUN apt-get update && apt-get install -y libpq-dev build-essential
RUN pip install --no-cache-dir -r /app/files/requirements.txt

COPY . /app/files

EXPOSE 8080
EXPOSE 5000

CMD ["python", "main.py"]