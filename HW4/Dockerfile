FROM python:3.9.7-alpine3.14

LABEL VERSION="1.0.0"
LABEL MAINTAINER="Andrii Bondariev"
LABEL EMAIL="andrii.bondariev@namecheap.com"
LABEL NAME="Web server"

WORKDIR /app

COPY db-server-app.py .

ENV MYSQL_USER=user
ENV MYSQL_ROOT_PASSWORD=password

RUN pip install mysql-connector-python

EXPOSE 8000

ENTRYPOINT [ "python", "db-server-app" ]