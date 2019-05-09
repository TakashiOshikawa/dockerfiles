FROM alpine:3.9.3 AS build_stage

RUN apk update && apk add openssh && apk add curl
RUN apk add git
RUN apk add htop
WORKDIR /tmp
RUN touch ttt.txt
RUN echo "multistagebuild copy from build_stage" >> ttt.txt

# マルチステージビルド
FROM alpine:3.9.3

WORKDIR /app

COPY --from=build_stage /tmp/ttt.txt /app/ttt_cp.txt

CMD ["cat", "/app/ttt_cp.txt"]

