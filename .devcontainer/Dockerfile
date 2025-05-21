FROM mcr.microsoft.com/devcontainers/python:1-3.12

RUN apt-get update && apt-get install -y \
    build-essential \
    vim

WORKDIR /workspace
COPY . .
RUN pip install uv && \
    uv init && \
    uv add -r requirements.txt

RUN git config --global core.editor 'vim'
RUN echo 'export EDITOR=vim' >> $HOME/.bashrc
RUN echo 'export VISUAL=vim' >> $HOME/.bashrc
RUN echo 'export TZ=Asia/Seoul' >> $HOME/.bashrc
