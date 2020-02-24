FROM richarvey/nginx-php-fpm:latest

ADD feed-updater.conf /etc/supervisor/conf.d/

RUN cd /var/www/html && \
    git clone --depth 20 https://git.tt-rss.org/fox/tt-rss.git