FROM takashioshikawa/centos6base

WORKDIR /tmp

RUN yum install -y epel-release
RUN yum install -y nodejs
RUN yum install -y npm --enablerepo=epel

RUN which npm

CMD /bin/bash
