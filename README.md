# sample-golang-packaging-gom
Sample Golang packaging (gom)

```
$ go version
go version go1.5.1 darwin/amd64
```

```
$ echo $GO15VENDOREXPERIMENT
1
$ go get github.com/mattn/gom
$ git clone git@github.com:achiku/sample-golang-packaging-gom.git && cd sample-golang-packaging-gom
$ gom install
$ find vendor -type d -maxdepth 2
vendor
vendor/github.com
vendor/github.com/fatih
vendor/github.com/mattn
vendor/github.com/shiena
vendor/pkg
vendor/pkg/darwin_amd64
$ gom run main.go  # it fails
$ gom build  # it fails
```


```
$ mkdir vendor/src
$ mv vendor/github.com vendor/src
$ gom run main.go
Hello, world!
$ gom build  # it succeeds
```
