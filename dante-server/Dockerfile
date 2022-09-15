# Other danted Dockefiles:
# https://github.com/adegtyarev/docker-dante
# https://github.com/wernight/docker-dante

FROM debian:bullseye-slim

ENV TZ="Europe/Moscow"

RUN apt-get update -y

RUN apt-get install -y --no-install-recommends mc # for debug

RUN apt-get install -y --no-install-recommends dante-server

RUN mv /etc/danted.conf /etc/danted.conf.original

COPY danted.conf /etc/danted.conf

ARG USER_NAME
ARG PASSWORD
RUN useradd -M ${USER_NAME} && echo ${USER_NAME}:${PASSWORD} | chpasswd

EXPOSE 1080
CMD danted