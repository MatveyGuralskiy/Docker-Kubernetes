#---------Docker file created by Matvey Guralskiy---------
#
#----GitHub profile https://github.com/MatveyGuralskiy----

FROM ubuntu:latest

ENV MY_USER=Matvey_Guralskiy

RUN mkdir -p /home/app

COPY ./text/ /home/app

CMD ["cat","/home/app/text.txt"]
