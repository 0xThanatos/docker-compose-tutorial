FROM php:7.4.10-fpm
WORKDIR "/app"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y && \
    apt-get install git -y

# Install Redis
# RUN cd /tmp & git clone https://github.com/phpredis/phpredis.git && \
#     cd phpredis && \
#     phpize && \
#     ./configure && \
#     make && make install

# RUN touch /usr/local/etc/php/conf.d/redis.ini && \
#     echo 'extension=redis.so' > /usr/local/etc/php/conf.d/redis.ini

# Install Swoole
# RUN cd /tmp && git clone https://github.com/swoole/swoole-src.git && \
#     cd swoole-src  && \
#     phpize && \
#     ./configure && \
#     make && make install

# RUN touch /usr/local/etc/php/conf.d/swoole.ini && \
#     echo 'extension=swoole.so' > /usr/local/etc/php/conf.d/swoole.ini

# Install selected extensions and other stuff
RUN apt-get update && \
    apt-get install -y apt-utils libpng-dev libpq-dev zlib1g-dev && \
    docker-php-ext-install \
    mysqli pdo pdo_mysql