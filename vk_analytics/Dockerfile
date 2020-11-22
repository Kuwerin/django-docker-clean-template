# pull official base image
#3.9.0-alpine3.12
FROM python:3.9.0-slim
# set work directory
WORKDIR /code
# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
# install dependencies
RUN export CFLAGS=-Qunused-arguments
RUN export CPPFLAGS=-Qunused-arguments
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt
# copy project
COPY . .
