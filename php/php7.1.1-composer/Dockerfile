FROM takashioshikawa/centos6base

WORKDIR /tmp

# PHP install 7.0.12
RUN yum install -y epel-release
RUN rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
RUN yum install -y --enablerepo=remi,remi-php71 php php-devel php-mbstring php-pdo php-gd php-opcache php-mcrypt php-mysqlnd php-phpunit-PHPUnit php-pecl-xdebug

# composer install
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/bin/composer

CMD /bin/bash
