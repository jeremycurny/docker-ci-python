FROM python:3-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN  \
    apt-get update \
    && apt-get install -y git rsync sshpass unzip zip \
    && apt-get clean autoclean \
    && apt-get autoremove
    
RUN \
    pip install awscli

RUN \
    mkdir -p /root/.ssh \
    && chmod 700 /root/.ssh \
    && echo "" > /root/.ssh/known_hosts
