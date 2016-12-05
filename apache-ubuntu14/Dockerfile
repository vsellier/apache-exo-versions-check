FROM ubuntu:14.04

RUN apt-get update && apt-get install -y apache2
RUN a2enmod proxy_http proxy_wstunnel

EXPOSE 80

CMD apachectl -d /etc/apache2 -f /etc/apache2/apache2.conf -e info -DFOREGROUND
