FROM jupyter/datascience-notebook
MAINTAINER Diego Pinheiro diegompin@gmail.com

COPY ./docker/mhs_jupyter/requirements.txt requirements.txt

#USER root
#RUN apt-get -y update && apt-get -y install build-essential libxml2-dev zlib1g-dev python-dev pkg-config libffi-dev libcairo-dev libtool
#
#RUN mkdir -p /usr/share/man/man1 && \
#    apt-get update -y && \
#    apt-get install -y openjdk-8-jdk
#
#USER $NB_UID

RUN ["pip", "install", "--user", "-r",  "requirements.txt"]

WORKDIR .
COPY ./ ./
ENV PYTHONPATH "${PYTONPATH}:./"

