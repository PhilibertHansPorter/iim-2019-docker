FROM httpd:latest


RUN echo 'LoadModule proxy_module modules/mod_proxy.so' >> /usr/local/apache2/conf/httpd.conf
RUN echo 'LoadModule proxy_fcgi_module modules/mod_proxy_fcgi.so' >> /usr/local/apache2/conf/httpd.conf
RUN echo 'Include conf/extra/httpd-vhosts.conf' >> /usr/local/apache2/conf/httpd.conf

RUN rm -rf /usr/local/apache2/htdocs/index.html
ADD index.php /usr/local/apache2/htdocs/index.php

ADD config/httpd-vhosts.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf