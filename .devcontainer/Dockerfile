FROM mcr.microsoft.com/devcontainers/python:1-3.12

RUN apt-get update && apt-get install -y \
    build-essential \
    vim

COPY . .

RUN pip install uv && \
    uv init && \
    uv add -r requirements.txt

WORKDIR /workspace

CMD ["/bin/bash", ".devcontainer/post-script"]