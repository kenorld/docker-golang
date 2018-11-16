FROM ubuntu:18.04

ENV GOLANG_VERSION 1.11.1
RUN apt update && apt install -y git subversion mercurial ca-certificates curl && \
    curl -O https://dl.google.com/go/go$GOLANG_VERSION.linux-amd64.tar.gz && \
    tar xf go$GOLANG_VERSION.linux-amd64.tar.gz --directory /usr/local && \
    rm go$GOLANG_VERSION.linux-amd64.tar.gz

ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
WORKDIR $GOPATH