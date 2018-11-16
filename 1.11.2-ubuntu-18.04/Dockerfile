FROM ubuntu:18.04

ENV GOLANG_VERSION 1.11.2
RUN apt update && apt install -y git subversion mercurial ca-certificates curl && \
    curl -sSL https://dl.google.com/go/go$GOLANG_VERSION.linux-amd64.tar.gz \
    tar -v -C /usr/local -xz

ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
WORKDIR $GOPATH