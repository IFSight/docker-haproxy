FROM fulcrum/centos
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

RUN echo "Cache bust 201604291406" && \
    groupadd -g 1971 haproxy && useradd -d /var/lib/haproxy -g haproxy -M -n -s /sbin/nologin -u 1971 haproxy && \
    rpm --rebuilddb && \
    yum --noplugins -y install haproxy && \
    yum --noplugins upgrade -y && \
    package-cleanup --dupes && \
    package-cleanup --cleandupes && \
    yum clean all    

ENTRYPOINT ["/usr/sbin/haproxy"]
CMD ["-f","/etc/haproxy/haproxy.cfg","-p","/var/run/haproxy.pid"]
