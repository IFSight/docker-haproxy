FROM haproxy:1.6-alpine
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

RUN apk update && apk upgrade && \
    adduser -s /sbin/nologin -D -h /dev/null -H haproxy

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["haproxy", "-f", "/etc/haproxy/haproxy.cfg"]
