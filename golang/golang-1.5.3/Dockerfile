
FROM takashioshikawa/centos6base

MAINTAINER "takashioshikawa" <abr3tks5200@gmail.com>


WORKDIR /tmp

RUN wget https://storage.googleapis.com/golang/go1.5.3.linux-amd64.tar.gz
RUN tar -C /usr/local -xzf go1.5.3.linux-amd64.tar.gz

ENV PATH $PATH:/usr/local/go/bin
ENV GOPATH $HOME/go
ENV PATH $PATH:$GOPATH/bin

RUN which go

RUN go get github.com/motemen/gore
RUN go get github.com/nsf/gocode
RUN go get github.com/k0kubun/pp
RUN go get golang.org/x/tools/cmd/godoc

RUN which gore

CMD /bin/bash

