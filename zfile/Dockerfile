FROM stilleshan/alpine-openjdk-8-headless:2021-06-11
MAINTAINER Stille <stille@ioiox.com>

ENV VERSION 3.2

WORKDIR /root

RUN wget https://github.com/zhaojun1998/zfile/releases/download/${VERSION}/zfile-${VERSION}.war \
    && mkdir zfile && unzip zfile-${VERSION}.war -d zfile && rm -rf zfile-${VERSION}.war \
    && chmod +x ~/zfile/bin/*.sh

EXPOSE 8080

CMD sh ./zfile/bin/start.sh && tail -f /dev/null

