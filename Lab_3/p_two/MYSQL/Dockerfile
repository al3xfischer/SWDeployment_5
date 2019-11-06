FROM debian:jessie

LABEL maintainer="103039@fhwn.ac.at"

USER root

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
RUN systemctl status mysql
# RUN mysql_secure_installation