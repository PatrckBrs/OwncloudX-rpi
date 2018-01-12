# Dockerfile Raspberry Pi Nginx
FROM hypriot/rpi-alpine-scratch:latest

RUN adduser nginx -D -H -u 1000 -s /sbin/nologin

ADD ./owncloud-script.sh /tmp/

CMD ["/tmp/owncloud-script.sh"]
