FROM php:7.2-fpm

LABEL maintainer="Stel000"
LABEL email="kkcyc1996@gmail.com"

RUN apt-get update && apt-get install -y \
    wget \
    unzip \
    git

RUN pecl install redis-5.1.1 \
    && pecl install igbinary-3.0.1 \
    && docker-php-ext-enable redis igbinary

RUN cd /var/www \
    && rm -rf ./html \
    && git clone https://github.com/a54552239/pearProjectApi \
    && mv ./pearProjectApi ./html \
    && cd html \
    && wget https://vilson-static.oss-cn-shenzhen.aliyuncs.com/common/vendor.zip \
    && unzip vendor.zip