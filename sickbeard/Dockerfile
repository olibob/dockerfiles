FROM centos:7

VOLUME /config
VOLUME /media

RUN yum -y -q update

RUN yum -y -q install git python-cheetah;\
    yum clean all;\
    git clone https://github.com/midgetspy/Sick-Beard.git /opt

EXPOSE 8081

ENTRYPOINT ["/usr/bin/python", "/opt/SickBeard.py", "--datadir=/config"]
