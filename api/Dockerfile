FROM python:3.8.3-alpine

WORKDIR /app
COPY . .
RUN \
 apk add --no-cache postgresql-libs && \
 apk add --no-cache --virtual .build-deps gcc musl-dev postgresql-dev && \
 python3 -m pip install -r requirements.txt --no-cache-dir && \
 pip install -r ./requirements.txt



EXPOSE 3050

CMD ["python", "index.py"]

