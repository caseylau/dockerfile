# from https://hub.docker.com/_/drupal?tab=tags
FROM drupal:8.6-fpm

# Install redis
RUN pecl install redis -y && docker-php-ext-enable redis

# drush command
ENV DRUSH_VERSION 0.6.0

RUN curl -fsSL -o /usr/local/bin/drush "https://github.com/drush-ops/drush-launcher/releases/download/$DRUSH_VERSION/drush.phar" && \
    chmod +x /usr/local/bin/drush

# drupal command
RUN curl https://drupalconsole.com/installer -L -o drupal.phar && \
    mv drupal.phar /usr/local/bin/drupal && \
    chmod +x /usr/local/bin/drupal

# install nessarary software
RUN apt-get update; \
    apt-get install -y vim mariadb-client
