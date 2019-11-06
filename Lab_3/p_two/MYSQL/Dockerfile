FROM debian:jessie

LABEL maintainer="103039@fhwn.ac.at"
USER root
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
COPY sec.sh sec.sh
RUN ./sec.sh
EXPOSE 3306 
CMD ["mysqld","--skip-grant"]