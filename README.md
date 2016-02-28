# Dockerfile centos7php70u

## Summary

This image is based on CentOS 7, PHP 7.0 from IUS Community repo sponsored by Rackspace and  Nginx 1.8.0 community platform.

It relies on Supervisord to retain Nginx and PHP-FPM up. PHP-FPM on the regular port 9000.  

## How to use

Create a Docker file as: 

    FROM ernestova/centos7php56u
    ADD . /var/www/html
    EXPOSE 80
    CMD ["/usr/local/bin/start.sh"]
    
It will use a nginx virtualhost as defined on files/default.conf
