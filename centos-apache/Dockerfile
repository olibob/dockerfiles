FROM centos:7
RUN yum -y -q update
RUN yum -y -q install httpd mod_ssl openssl mod_proxy_html

EXPOSE 80
EXPOSE 443

VOLUME /var/www/html
VOLUME /var/log/httpd

ENTRYPOINT ["httpd", "-D", "FOREGROUND"]
