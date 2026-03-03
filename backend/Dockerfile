# backend/Dockerfile

FROM python:3.11-slim

WORKDIR /app

COPY dependencies.txt .

RUN pip install --upgrade pip setuptools wheel
RUN pip install setuptools==69.5.1
RUN pip install -r dependencies.txt

COPY . .

ENV PYTHONUNBUFFERED=1

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
