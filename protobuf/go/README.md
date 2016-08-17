# protobuf-go

[![Docker Stars](https://img.shields.io/docker/stars/gnhuy91/protobuf-go.svg)][hub] [![Docker Pulls](https://img.shields.io/docker/pulls/gnhuy91/protobuf-go.svg)][hub] [![Image Size](https://images.microbadger.com/badges/image/gnhuy91/protobuf-go.svg)](https://microbadger.com/images/gnhuy91/protobuf-go "Get your own image badge on microbadger.com")

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
