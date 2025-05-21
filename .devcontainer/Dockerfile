FROM mcr.microsoft.com/devcontainers/python:1-3.12

RUN apt-get update && apt-get install -y \
    build-essential \
    vim

WORKDIR /workspaces
COPY . .
RUN pip install uv

RUN git config --global core.editor 'vim'
RUN echo 'export EDITOR=vim' >> $HOME/.bashrc
RUN echo 'export VISUAL=vim' >> $HOME/.bashrc
RUN echo 'export TZ=Asia/Seoul' >> $HOME/.bashrc
