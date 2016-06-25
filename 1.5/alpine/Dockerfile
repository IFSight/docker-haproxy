FROM haproxy:1.5-alpine
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

RUN echo "Cache bust 201606232004" && \
    apk update && apk upgrade && \
    adduser -s /sbin/nologin -D -h /dev/null -H haproxy

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["haproxy", "-f", "/etc/haproxy/haproxy.cfg"]
