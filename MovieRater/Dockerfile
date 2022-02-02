# pull the official base image
FROM python:latest

# set work directory
WORKDIR /django

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install dependencies
RUN pip install --upgrade pip
COPY ./requirements.txt /django
RUN pip install -r requirements.txt

# copy project
COPY . /django

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]