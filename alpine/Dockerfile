FROM rainist/scala:2.13.1-alpine

LABEL maintainer="engineering@rainist.com"

ENV SBT_VERSION 1.3.8
ENV SBT_HOME /usr/local/sbt

ENV PATH ${PATH}:${SBT_HOME}/bin

RUN curl -sL "https://github.com/sbt/sbt/releases/download/v$SBT_VERSION/sbt-$SBT_VERSION.tgz" | gunzip | tar -x -C /usr/local && \
    echo -ne "- with sbt $SBT_VERSION\n" >> /root/.built && \
    sbt sbtVersion
