
FROM takashioshikawa/centos6base

RUN yum install -y mysql-server

# MySQLが起動できるようにするために必要
RUN echo "NETWORKING=yes" > /etc/sysconfig/network

# /etc/my.cnfの設定
RUN echo "[mysqld]" > /etc/my.cnf && \
    echo "datadir=/var/lib/mysql" >> /etc/my.cnf && \
    echo "socket=/var/lib/mysql/mysql.sock" >> /etc/my.cnf && \
    echo "user=mysql" >> /etc/my.cnf && \
    echo "# Disabling symbolic-links is recommended to prevent assorted security risks" >> /etc/my.cnf && \
    echo "symbolic-links=0" >> /etc/my.cnf && \
    echo "character-set-server=utf8" >> /etc/my.cnf && \
    echo "[mysqld_safe]" >> /etc/my.cnf && \
    echo "log-error=/var/log/mysqld.log" >> /etc/my.cnf && \
    echo "pid-file=/var/run/mysqld/mysqld.pid" >> /etc/my.cnf && \
    echo "[client]" >> /etc/my.cnf && \
    echo "default-character-set=utf8" >> /etc/my.cnf

# ユーザ作成, 権限付与, DB作成
RUN /etc/init.d/mysqld start && \
    mysql -u root -e 'CREATE USER some_user@localhost IDENTIFIED BY "some_password"' && \
    mysql -u root -e 'GRANT ALL PRIVILEGES ON some_database.* TO some_user@localhost IDENTIFIED BY "some_password"' && \
    mysql -u root -e 'CREATE USER some_user@"%" IDENTIFIED BY "some_password"' && \
    mysql -u root -e 'GRANT ALL PRIVILEGES ON some_database.* TO some_user@"%"' && \
    mysql -u root -e 'create database some_database' && \
    /etc/init.d/mysqld stop

RUN /usr/bin/mysql_install_db

CMD /usr/bin/mysqld_safe

