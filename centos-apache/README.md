## centos-apache

A dockerfile for apache + php + php-mysql

Centos `7`

Apache `2.4.6`

PHP `5.4.16`

### Tags

Apache `2.4.6`, `latest`

### Ports

Standard `80` and `443`

### Volumes

`/var/www/html` and `/var/log/httpd`

### Usage

```bash
docker run -d --name apache -p 80:80 -p 443:443 olibob/apache
```

To run your local static files you could do

```bash
docker run -d --name mysite -p 80:80 -v $PWD/mysite:/var/www/html olibob/apache
```
