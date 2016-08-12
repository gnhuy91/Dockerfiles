# protobuf Go

[![Docker Stars](https://img.shields.io/docker/stars/gnhuy91/protobuf-go.svg)][hub] [![Docker Pulls](https://img.shields.io/docker/pulls/gnhuy91/protobuf-go.svg)][hub]

Go support for Protocol Buffers, inside a tiny (9 mb) Docker image.

# Usage

```sh
docker run --rm \
    -u $(id -u):$(id -g) \
    -v $PWD:/src:rw \
    -w /src \
    gnhuy91/protobuf-go \
    --go_out=. *.proto
```

[hub]: https://hub.docker.com/r/gnhuy91/protobuf-go/
