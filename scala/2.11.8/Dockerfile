
FROM takashioshikawa/java8

WORKDIR /tmp

# Scala install
RUN wget http://downloads.typesafe.com/scala/2.11.8/scala-2.11.8.tgz
RUN tar xvzf scala-2.11.8.tgz
RUN mkdir /usr/local/scala
RUN mv scala-2.11.8 /usr/local/scala
ENV PATH $PATH:/usr/local/scala/scala-2.11.8/bin

RUN echo $PATH
RUN which scala


# sbt install
RUN curl https://bintray.com/sbt/rpm/rpm | tee /etc/yum.repos.d/bintray-sbt-rpm.repo
RUN yum install -y sbt

# java 1.6 uninstall
RUN update-alternatives --set java /usr/lib/jvm/jre-1.8.0-openjdk.x86_64/bin/java
RUN alternatives --install /usr/bin/java java /usr/lib/jvm/jre-1.8.0-openjdk.x86_64/bin/java 16024

RUN which sbt


CMD /bin/bash

