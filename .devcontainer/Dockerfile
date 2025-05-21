FROM mcr.microsoft.com/devcontainers/python:1-3.12

RUN apt-get update && apt-get install -y \
    build-essential \
    vim

WORKDIR /workspace
COPY . .
RUN pip install uv && \
    uv init && \
    uv add -r requirements.txt

RUN /bin/bash .devcontainer/post-script

CMD ["uv", "run", "marimo", "edit"]