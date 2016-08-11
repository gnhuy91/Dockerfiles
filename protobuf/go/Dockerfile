FROM gnhuy91/protobuf
MAINTAINER Huy Giang <gnhuy91@gmail.com>

RUN mkdir -p /go/src /go/bin && \
    chmod -R 777 /go/bin

ENV GOPATH /go
ENV PATH $GOPATH/bin:$PATH

ENV BUILD_PACKAGES "git ca-certificates"

RUN apk add --update --no-cache $BUILD_PACKAGES go && \
    # Get Go grpc
    go get google.golang.org/grpc && \
    go get github.com/golang/protobuf/protoc-gen-go && \
    apk del $BUILD_PACKAGES && \
    rm -rf /var/cache/apk
