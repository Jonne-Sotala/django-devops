FROM python:3.9-alpine

WORKDIR /src/app/

RUN apk update && \
    apk add --virtual build-deps gcc python3-dev musl-dev && \
    apk add postgresql-dev

COPY . .

RUN pip install --upgrade pip
RUN pip install -r requirements.txt
RUN pip install psycopg2

ENTRYPOINT ["sh", "./entrypoint.sh"]
