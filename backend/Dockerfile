FROM python:3.12-alpine

WORKDIR /app

COPY app.py .

RUN addgroup -S backend_group && adduser -S backend_user -G backend_group

RUN chown backend_user:backend_group app.py

USER backend_user

EXPOSE 8080

CMD ["python", "app.py"]