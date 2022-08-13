# placekey

Unofficial port of the Python library [placekey-py](https://github.com/Placekey/placekey-py), not affiliated with the Placekey project.

## Install

```go
go get github.com/diegosz/placekey
```

This package requires **Go 1.18** or later.

## Prerequisites

This library depends on [uber/h3-go](https://github.com/uber/h3-go) and inherits the same [prerequisites](https://github.com/uber/h3-go#prerequisites). It requires [CGO](https://golang.org/cmd/cgo/) (```CGO_ENABLED=1```) in order to be built.

> If you see errors/warnings like "build constraints exclude all Go files...", then the cgo build constraint is likely disabled; try setting CGO_ENABLED=1 environment variable for your build step.

## References

- <https://www.placekey.io>
- <https://docs.placekey.io>
- <https://docs.placekey.io/Placekey_Encoding_Specification_White_Paper.pdf>
- <https://github.com/Placekey/placekey-py>
- <https://github.com/engelsjk/placekey-go>
- <https://github.com/ringsaturn/pk>
