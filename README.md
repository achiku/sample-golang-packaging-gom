# sample-golang-packaging-gom
Sample Golang packaging (gom with `GO15VENDOREXPERIMENT`)

- https://medium.com/@freeformz/go-1-5-s-vendor-experiment-fd3e830f52c3#.90n00wizr

```
$ go version
go version go1.5.1 darwin/amd64
```

```
$ echo $GO15VENDOREXPERIMENT
1
$ go get github.com/mattn/gom
$ cd $GOPATH/src/github.com/achiku
$ git clone git@github.com:achiku/sample-golang-packaging-gom.git 
$ cd sample-golang-packaging-gom
$ gom install
$ find vendor -type d -maxdepth 2
vendor
vendor/github.com
vendor/github.com/fatih
vendor/github.com/mattn
vendor/github.com/shiena
vendor/pkg
vendor/pkg/darwin_amd64
$ gom run main.go 
Hello, world!
$ go run main.go
Hello, world!
```
