FROM debian:jessie

RUN apt-get update 
RUN apt-get install wordpress -y
RUN mv /usr/share/wordpress/wp-config-sample.php /etc/wordpress/config-localhost.php
RUN cp -R /usr/share/wordpress/* /var/www/html/
#   php7.3-curl php-gd php-mbstring php-xml php-xmlrpc php-soap php-intl php-zip
# RUN apt-get install apache2 wordpress
ENTRYPOINT while true; do sleep 1000; done



EXPOSE 80