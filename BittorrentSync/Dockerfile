FROM centos
RUN yum -y -q update
RUN yum -y -q install tar gunzip
RUN curl -s -o /tmp/btsync.tar.gz  https://download-cdn.getsyncapp.com/stable/linux-x64/BitTorrent-Sync_x64.tar.gz
RUN cd /tmp; \
     tar xzf btsync.tar.gz btsync; \
     cp btsync /usr/local/bin; \
     chmod +x /usr/local/bin/btsync; \
     rm -f btsync.tar.gz

VOLUME /data

EXPOSE 3369/udp
EXPOSE 8888

ENTRYPOINT [ "btsync" , "--nodaemon" ]
CMD [ "--webui.listen", "0.0.0.0:8888" ]
