FROM python:3.9.7-alpine3.14 AS builder

LABEL VERSION="1.0.0"
LABEL MAINTAINER="Andrii Bondariev"
LABEL EMAIL="andrii.bondariev@namecheap.com"
LABEL NAME="Web server"

WORKDIR /app

COPY server-app.py .

RUN python3 source/server-app.py


FROM alpine:3.14.2

WORKDIR /app

COPY --from=builder /app/server-app .

EXPOSE 8080

ENTRYPOINT [ "./server-app" ]