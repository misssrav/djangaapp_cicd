FROM python:3.8-slim

WORKDIR /app

RUN apt-get update && apt-get install -y sqlite3 && apt-get clean

COPY requirements.txt /app
COPY devops /app

RUN pip install -r requirements.txt


ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




