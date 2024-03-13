FROM amazonlinux

RUN yum -y update && \
    yum -y install httpd && \
    yum -y install php && \
    mkdir /run/php-fpm

COPY custom.conf /etc/httpd/conf.d/custom.conf
COPY ./index.php /var/www/html/index.php

CMD ["/bin/sh", "-c", "/usr/sbin/php-fpm && /usr/sbin/httpd -D FOREGROUND"]
EXPOSE 80
