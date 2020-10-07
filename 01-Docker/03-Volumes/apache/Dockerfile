FROM ubuntu:16.04

RUN apt-get update

RUN apt-get install apache2 -y 

COPY hello.html /var/www/html/hello.html

EXPOSE 80

CMD ["/usr/sbin/apache2ctl" , "-D", "FOREGROUND"]
