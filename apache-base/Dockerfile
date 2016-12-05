FROM ubuntu:16.04

RUN apt-get update && apt-get install -y wget build-essential libpcre3-dev

ARG APACHE_VERSION

RUN cd / && wget http://archive.apache.org/dist/httpd/httpd-${APACHE_VERSION}.tar.gz && tar xvzf httpd-${APACHE_VERSION}.tar.gz && \
    wget http://archive.apache.org/dist/httpd/httpd-${APACHE_VERSION}-deps.tar.gz && tar xvzf httpd-${APACHE_VERSION}-deps.tar.gz && \
    cd /httpd-${APACHE_VERSION} && ./configure --enable-modules=all && make -j 4 && make install
EXPOSE 80

CMD /usr/local/apache2/bin/apachectl -d /usr/loca/apache2 -f /usr/local/apache2/conf/httpd.conf -e info -DFOREGROUND

