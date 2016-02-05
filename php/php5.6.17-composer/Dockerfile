
From takashioshikawa/centos6base

WORKDIR /tmp

# PHP install
RUN rpm -Uvh http://ftp.iij.ad.jp/pub/linux/fedora/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
RUN yum install -y --enablerepo=remi --enablerepo=remi-php56 php php-opcache php-devel php-mbstring php-mcrypt php-mysqlnd php-phpunit-PHPUnit php-pecl-xdebug php-pecl-xhprof

# composer install
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/bin/composer

CMD /bin/bash
