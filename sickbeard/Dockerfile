FROM centos:7

VOLUME /config
VOLUME /media

RUN yum -y -q update

RUN yum -y -q install git python-cheetah;\
    yum clean all;\
    git clone https://github.com/midgetspy/Sick-Beard.git /opt

# Revert to this commit to avoid bug in last commit 79cb8f207bef8613db9e47eb392666af059df3d0
RUN cd /opt; git checkout ff36290ba50a08d004b41cbcb8649645c324797a

EXPOSE 8081

ENTRYPOINT ["/usr/bin/python", "/opt/SickBeard.py", "--datadir=/config"]
