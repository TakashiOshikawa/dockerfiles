
FROM centos:6

MAINTAINER "takashioshikawa" <abr3tks5200@gmail.com>


RUN yum update -y
RUN yum install -y which
RUN yum install -y wget
RUN yum install -y tar
RUN yum install -y vim


RUN cd /tmp && wget http://sherkin.justhub.org/el6/RPMS/x86_64/justhub-release-2.0-4.0.el6.x86_64.rpm
RUN rpm -ivh /tmp/justhub-release-2.0-4.0.el6.x86_64.rpm
RUN yum install -y haskell && cd /


CMD which runghc && /bin/bash
