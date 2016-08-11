FROM gliderlabs/alpine:3.4
MAINTAINER Huy Giang <gnhuy91@gmail.com>

ENV PROTO_VERSION "v3.0.0"
ENV BUILD_PACKAGES "git curl build-base autoconf automake libtool"

RUN apk add --update --no-cache $BUILD_PACKAGES && \
    # Install protobuf
    git clone https://github.com/google/protobuf -b $PROTO_VERSION --depth 1 && \
    cd protobuf && \
    ./autogen.sh && \
    ./configure --prefix=/usr && \
    make -j 3 && \
    make check && \
    make install && \
    cd .. && \
    rm -rf protobuf && \
    # libstdc++ is required for running protobuf binary
    apk add --no-cache libstdc++ && \
    # Cleanup installed packages
    apk del $BUILD_PACKAGES && \
    rm -rf /var/cache/apk/*

ENTRYPOINT ["protoc"]
