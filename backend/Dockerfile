FROM python:3.9
RUN echo "${DOCKER_USERNAME}" > /tmp/docker_username && chmod 0400 /tmp/docker_username
WORKDIR /app
RUN pip install gunicorn==20.1.0
COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir
COPY . .
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]