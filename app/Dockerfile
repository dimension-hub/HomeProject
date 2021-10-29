# the image on the basis of which we create the container
FROM python:3.9.7-alpine

# working directory inside the project
WORKDIR /usr/src/app

# environment variables for python
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1


# Install dependencies for Postgre
RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev


# install dependencies
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# copy the contents of the current folder to the container
COPY . .
