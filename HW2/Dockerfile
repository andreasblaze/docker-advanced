FROM python:3.9.7-alpine3.14

LABEL VERSION="1.0.0"
LABEL MAINTAINER="Andrii Bondariev"
LABEL EMAIL="andrii.bondariev@namecheap.com"
LABEL NAME="Web server"

WORKDIR /app

COPY main.py .

EXPOSE 8080

ENTRYPOINT [ "python" ]
CMD [ "main.py" ]