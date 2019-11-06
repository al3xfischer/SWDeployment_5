FROM debian:jessie

ENV DB_NAME=unknown
ENV DB_USER=root
ENV DB_PASSWORD=rootpw
ENV DB_HOST=unknown

RUN apt-get update 
RUN apt-get install wordpress -y
RUN mv /var/www/html/index.html /var/www/html/index.bak
COPY wp-config.php /etc/wordpress/config-localhost.php
# RUN mv /usr/share/wordpress/wp-config-sample.php /etc/wordpress/config-localhost.php
RUN cp -R /usr/share/wordpress/* /var/www/html/
#   php7.3-curl php-gd php-mbstring php-xml php-xmlrpc php-soap php-intl php-zip
# RUN apt-get install apache2 wordpress
ENTRYPOINT service apache2 start && DB_NAME=${DB_NAME} DB_USER=${DB_USER} DB_PASSWORD=${DB_PASSWORD} DB_HOST=${DB_HOST} && tail -f /dev/null

EXPOSE 80