FROM python:3.7-alpine

ENV PYTHONUNBUFFERED=1

# Install requirements
ENV DEV_PKGS='openssh git'
ENV PIP_PACKAGES='flake8 bandit autopep8'

RUN mkdir -p ~/.ssh && \
    export PATH="/root/.local/bin:$PATH" && \
    apk add --no-cache --virtual .build-deps $DEV_PKGS && \
    python -m pip install -U $PIP_PACKAGES
