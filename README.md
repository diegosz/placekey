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

## FIXME

ToGeoBoundary is not working as expected, at least with pentagon of resolution 1. I did not verified further cases.

Cell `81c23ffffffffff` should return something like:

```csv
-42.26111252924078, -57.99532236959882
-41.11855205411782, -54.9141712970285
-40.22211498519526, -53.8497030003696
-37.6912453875986, -54.414765681393625
-36.64293584360804, -55.16400420796509
-36.2052826312824, -58.30984616813221
-36.39482705911914, -59.78817573003526
-38.614966841835646, -61.417114959977745
-39.80088198666685, -61.70280552750996
-41.71719450086273, -59.44411918804661
```

But returns this boundary:

```csv
-39.10059112493233, -57.70011129193584
-39.10035523525216, -57.69953126249852
-39.099764140502096, -57.69941956740003
-39.09949904241487, -57.70010944253918
-39.09992629443885, -57.70064751000666
-39.100427284162706, -57.700537659888724
```
