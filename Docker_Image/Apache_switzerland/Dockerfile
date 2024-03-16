FROM amazonlinux

RUN yum -y update && \
    yum -y install httpd

COPY ./index.html /var/www/html/index.html
COPY ./CSS/styles.css /var/www/html/CSS/
COPY ./background/Background.jpg /var/www/html/background/
COPY ./images/* /var/www/html/images/

CMD ["/usr/sbin/httpd" , "-D" , "FOREGROUND"]

EXPOSE 80
