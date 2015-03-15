FROM centos:7
RUN yum -y -q update
RUN yum -y -q install httpd php php-mysql

EXPOSE 80
EXPOSE 443

VOLUME /var/www/html
VOLUME /var/log/httpd

ENTRYPOINT ["httpd", "-D", "FOREGROUND"]
