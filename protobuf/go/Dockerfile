FROM gnhuy91/protobuf

ENV BUILD_PACKAGES "go git ca-certificates"

RUN apk add --update --no-cache $BUILD_PACKAGES && \
    rm -rf /var/cache/apk/*

RUN mkdir -p /go/src /go/bin && \
    chmod -R 777 /go/bin

ENV GOPATH /go
ENV PATH /go/bin:$PATH

# Get Go grpc
RUN go get google.golang.org/grpc
RUN go get github.com/golang/protobuf/protoc-gen-go
