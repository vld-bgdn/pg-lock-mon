#FROM python:3.9-slim
#FROM python:3-alpine
FROM python:3

WORKDIR /usr/src/app

#RUN apk update
#RUN apk add postgresql-dev gcc python3-dev musl-dev

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY db.py .
COPY deadlock_test.py .

CMD [ "python", "-u", "deadlock_test.py" ]