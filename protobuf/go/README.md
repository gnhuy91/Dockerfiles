# protobuf Go

Go support for Protocol Buffers, inside a tiny Docker image.

# Usage

```sh
docker run --rm \
    -u $(id -u):$(id -g) \
    -v $(PWD):/src:rw \
    -w /src \
    gnhuy91/protobuf-go \
    --go_out=. *.proto
```
