
FROM takashioshikawa/java8

WORKDIR /tmp

RUN wget http://downloads.typesafe.com/scala/2.11.7/scala-2.11.7.tgz
RUN tar xvzf scala-2.11.7.tgz
RUN mkdir /usr/local/scala
RUN mv scala-2.11.7 /usr/local/scala
#RUN export PATH=$PATH:/usr/local/scala/scala-2.11.7/bin
ENV PATH $PATH:/usr/local/scala/scala-2.11.7/bin
RUN echo $PATH

RUN which scala

CMD /bin/bash

