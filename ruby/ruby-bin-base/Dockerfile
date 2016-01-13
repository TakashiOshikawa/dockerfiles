
FROM takashioshikawa/centos6base

WORKDIR ~/

RUN yum install -y gcc-c++ glibc-headers openssl-devel readline libyaml-devel readline-devel zlib zlib-devel
RUN yum install -y bzip2

RUN wget http://ftp.ruby-lang.org/pub/ruby/2.2/ruby-2.2.4.tar.gz
RUN tar -xzvf ruby-2.2.4.tar.gz
WORKDIR ruby-2.2.4
RUN ./configure --disable-install-doc
RUN make
RUN make install
RUN gem install bundler

CMD /bin/bash

