#---------Docker file created by Matvey Guralskiy---------
#
#----GitHub profile https://github.com/MatveyGuralskiy----

FROM ubuntu:latest

RUN apt-get -y update
RUN apt-get -y install apache2

RUN echo 'Basic Website by Apache with Docker' > /var/www/html/index.html

CMD ["/usr/sbin/apache2ctl","-DFOREGROUND"]
EXPOSE 80
