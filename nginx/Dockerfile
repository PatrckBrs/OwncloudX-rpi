# Dockerfile Raspberry Pi Nginx
FROM hypriot/rpi-alpine-scratch:latest

RUN adduser nginx -D -H -u 1000 -s /sbin/nologin

RUN apk update && \
    apk add nginx

# Set whole bunch of stuff
RUN mkdir -p /var/www /run/nginx

# Ports
EXPOSE 80 443

# Boot up Nginx when container is started
CMD ["nginx", "-g", "daemon off;"]
