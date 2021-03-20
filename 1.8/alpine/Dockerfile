FROM haproxy:1.8-alpine
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

ENV BUILDDATE 202103192005

RUN apk update && apk upgrade && apk add socat

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["haproxy", "-f", "/etc/haproxy/haproxy.cfg"]
