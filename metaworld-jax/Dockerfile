FROM python:3.12.5-slim
LABEL maintainer="me@rainx0r.dev"

RUN apt-get update && apt install -y --no-install-recommends git libglfw3 libglfw3-dev g++
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /usr/src/app
COPY requirements.txt ./
RUN uv pip install --no-cache-dir --upgrade --pre --system -r requirements.txt

ENTRYPOINT ["python"]

