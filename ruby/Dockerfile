
FROM takashioshikawa/centos6base

WORKDIR ~/

RUN yum install -y gcc make openssl-devel libffi-devel
RUN yum install -y bzip2
RUN yum install -y readline-devel

RUN git clone https://github.com/sstephenson/rbenv.git ~/.rbenv

ENV PATH $PATH:~/.rbenv/bin
RUN echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
RUN exec $SHELL -l

RUN git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

RUN rbenv install 2.2.4
RUN rbenv global 2.2.4

CMD /bin/bash
