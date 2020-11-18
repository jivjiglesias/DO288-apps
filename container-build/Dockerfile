# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
RUN sed -i 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf && \ 
    chgrp -R 0 /var/run/httpd /var/log/httpd && \
    chmod -R g=u /var/run/httpd /var/log/httpd 
EXPOSE 8080
user 1001
CMD httpd -D FOREGROUND

