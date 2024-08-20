FROM ghcr.io/nvidia/jax:jax-2024-08-19
LABEL maintainer="me@evangelos.ai"

RUN apt-get update && apt install -y --no-install-recommends git libglfw3 libglfw3-dev

WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir --upgrade -r requirements.txt

ENTRYPOINT ["python"]
