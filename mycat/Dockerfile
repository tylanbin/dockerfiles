FROM openjdk:7

# install mycat-1.6
ADD http://dl.mycat.io/1.6-RELEASE/Mycat-server-1.6-RELEASE-20161028204710-linux.tar.gz /usr/local
RUN cd /usr/local && tar -zxvf Mycat-server-1.6-RELEASE-20161028204710-linux.tar.gz

# default port in /usr/local/mycat/conf/server.xml
EXPOSE 8066 9066

CMD /usr/local/mycat/bin/mycat console
