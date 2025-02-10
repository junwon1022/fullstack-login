FROM python:3.10

WORKDIR /app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV DJANGO_SECRET_KEY=your_secret_key
ENV DATABASE_URL=postgres://myuser:mypassword@db:5432/mydatabase

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
