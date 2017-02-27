FROM takashioshikawa/centos6base

WORKDIR /tmp

RUN curl --silent --location https://rpm.nodesource.com/setup_6.x | bash -
RUN yum remove -y nodejs npm
RUN yum install -y nodejs

RUN which npm

CMD /bin/bash
