FROM centos:7

VOLUME /config
VOLUME /media

RUN yum -y -q update

RUN yum -y -q install git python-cheetah wget tar;\
    yum clean all;\
    cd /tmp; wget --quiet https://github.com/midgetspy/Sick-Beard/archive/build-507.tar.gz; \
    tar xzf build-507.tar.gz; \
    cp -r Sick-Beard-build-507/* /opt/ ;\
    rm -rf Sick-Beard-build-507 build-507.tar.gz

EXPOSE 8081

ENTRYPOINT ["/usr/bin/python", "/opt/SickBeard.py", "--datadir=/config"]
