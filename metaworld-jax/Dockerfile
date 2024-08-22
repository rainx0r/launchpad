FROM python:3.12.5-slim
LABEL maintainer="me@evangelos.ai"

RUN apt-get update && apt install -y --no-install-recommends git python3-pip libglfw3 libglfw3-dev

WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir --upgrade -r requirements.txt

ENTRYPOINT ["python"]

