FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    bind9

COPY named.conf /etc/bind/named.conf
COPY db.example.com /etc/bind/db.example.com

EXPOSE 53/udp 53/tcp

CMD ["named", "-g", "-c", "/etc/bind/named.conf"]
