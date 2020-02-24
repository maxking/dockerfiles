FROM richarvey/nginx-php-fpm:latest

ADD feed-updater.conf /etc/supervisor/conf.d/

RUN /usr/local/bin/docker-php-ext-configure pcntl && \
    /usr/local/bin/docker-php-ext-install pcntl && \
    cd /var/www/html && \
    git clone --depth 20 https://git.tt-rss.org/fox/tt-rss.git && \
    git clone --depth 10 https://github.com/levito/tt-rss-feedly-theme /tmp/feedly-theme && \
    cp -r /tmp/feedly-theme/feedly* tt-rss/themes.local/