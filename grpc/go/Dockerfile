FROM golang:1.6

MAINTAINER Huy Giang <gnhuy91@gmail.com>

ENV PROTO_VERSION v3.0.0
ENV BUILD_PACKAGES 'git curl unzip build-essential autoconf libtool'

RUN apt-get update && \
    apt-get -y install ${BUILD_PACKAGES} && \
    # Install protobuf from source
    git clone https://github.com/google/protobuf.git && \
    cd protobuf && \
    git checkout tags/${PROTO_VERSION} && \
    ./autogen.sh && \
    ./configure && \
    make && \
    make install && \
    ldconfig && \
    make clean && \
    cd .. && \
    rm -r protobuf && \
    # Get golang grpc
    go get google.golang.org/grpc && \
    go get github.com/golang/protobuf/protoc-gen-go && \
    # cleanup
    apt-get remove --purge -y ${BUILD_PACKAGES} $(apt-mark showauto) && \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["protoc"]
