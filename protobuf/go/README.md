# protobuf Go Docker image

Go support for Protocol Buffers, inside a tiny Docker image.

# Usage

```console
docker run --rm \
    -u $(shell id -u):$(shell id -g) \
    -v $(PWD):/src:rw \
    -w /src \
    gnhuy91/protobuf-go \
    --go_out=. *.proto
```
