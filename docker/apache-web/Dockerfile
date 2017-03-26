#############################################
## Dockerfile to build an image to apache2 ##
#############################################
FROM ubuntu:14.04
MAINTAINER Milenio X <jnkmiloq@gmail.com>
# Install apache2 package
RUN apt-get update && \
    apt-get install -y apache2 && \
    apt-get clean
# Set the log directory PATH
ENV APACHE_LOG_DIR /var/log/apache2
# Expose the volume
VOLUME /var/www/html/
# Expose ports
EXPOSE 80
# Launch apache2 server in the foreground
ENTRYPOINT ["usr/sbin/apache2ctl", "-D", "FOREGROUND"]