# protobuf

[![Image Size](https://images.microbadger.com/badges/image/gnhuy91/protobuf.svg)](https://microbadger.com/images/gnhuy91/protobuf "Get your own image badge on microbadger.com") [![Docker Stars](https://img.shields.io/docker/stars/gnhuy91/protobuf.svg)][hub] [![Docker Pulls](https://img.shields.io/docker/pulls/gnhuy91/protobuf.svg)][hub]

Tiny (7 mb) Protocol Buffers 3 Docker image, powered by Alpine Linux.

# Usage

```sh
# Print protobuf help message
docker run -it --rm \
    gnhuy91/protobuf --help

# Use current folder for input and output
docker run -it --rm -v $PWD:/src:rw \
    gnhuy91/protobuf --cpp_out=. *.proto

# If you ran into problems with user uid and gid
docker run -it --rm \
    -u $(id -u):$(id -g) \
    -v $PWD:/src:rw \
    -w /src \
    gnhuy91/protobuf --cpp_out=. *.proto
```

[hub]: https://hub.docker.com/r/gnhuy91/protobuf/
