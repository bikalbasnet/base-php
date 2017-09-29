FROM php:7.1.9-fpm

RUN DEBIAN_FRONTEND=noninteractive \

    #Install Composer
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
    && chmod +x /usr/local/bin/composer

#COPY ./conf/www.conf /usr/local/etc/php-fpm.d/
#COPY ./conf/php.ini /usr/local/etc/php/
#COPY ./conf/xdebug.ini /usr/local/etc/php/conf.d/

COPY ./docker-entrypoint.sh /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["php-fpm"]

WORKDIR /var/www
