FROM python:3.9

WORKDIR /app

RUN pip install gunicorn==20.1.0

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

#GPT
# RUN apt-get update && apt-get install -y iputils-ping


CMD ["gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]



# FROM python:3.9

# WORKDIR /app

# COPY requirements.txt .

# RUN pip install -r requirements.txt --no-cache-dir

# COPY . .

# CMD ["python", "manage.py", "runserver", "0:8000"]