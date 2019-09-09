#This is a dockefile for mycart micro service layer
FROM centos:7
MAINTAINER abdullamancheri@gmail.com
RUN yum -y update 
ADD config /opt
RUN yum -y install `cat /opt/packages`
RUN yum -y install `cat /opt/my-packages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test MY_DB_HOST_WRITE=test MY_DB_HOST_READE=test MY_DB_NAME=test MY_DB_USER=test MY_DB_PASS=test
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]