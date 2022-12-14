<!-- BEGIN __DO_NOT_INCLUDE__ -->
<p align="center"><img src="https://gist.githubusercontent.com/thazelart/5be06c101f53079b9914d6efd867e690/raw/4ca768dbcd319dafef4aa7c2511bfa2b580858db/golang-grpc-template.png" alt="Logo" height="120" /></p>
<!-- END __DO_NOT_INCLUDE__ -->
<h1 align="center"> golang-grpc-template</h1>

<p align="center">
  <a href="https://github.com/gojp/goreportcard/blob/master/LICENSE" rel="nofollow"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="License Apache 2.0" style="max-width:100%;"></a>
  <a href="https://pkg.go.dev/github.com/thazelart/golang-grpc-template" rel="nofollow"><img src="https://pkg.go.dev/badge/github.com/thazelart/golang-grpc-template.svg" alt="Go reference" style="max-width:100%;"></a>
  <a href="https://goreportcard.com/report/github.com/thazelart/golang-grpc-template" rel="nofollow"><img src="https://goreportcard.com/badge/github.com/thazelart/golang-grpc-template" alt="Go report card" style="max-width:100%;"></a>
</p>
<br/>

An opinionated template for new Golang gRPC projects.

<!-- BEGIN __DO_NOT_INCLUDE__ -->

This repository is based on [golang-cli-template](https://github.com/thazelart/golang-cli-template).

It includes:

- The base of a cli using `spf13/cobra` (including the `version` command)
- Everything needed to test using `stretchr/testify`
- GitHub actions including release using `goreleaser/goreleaser`
- The optimized and secured Dockerfile
- Templating engine using `rantav/go-archetype`

More to come.

## Init your own project using that template

We are using [rantav/go-archetype](https://github.com/rantav/go-archetype) to enable the creation of new projects from that template.

```bash
$ go install github.com/rantav/go-archetype@latest

$ go-archetype transform --transformations .go-archetype.yaml --source . --destination /path/to/destination
# answer the questions

$ cd /path/to/destination
# init your git repository and you're done.
```

Enjoy developing your awesome cli.

<!-- END __DO_NOT_INCLUDE__ -->

## Install

### Manual install

```bash
$ git clone github.com/thazelart/golang-grpc-template
$ cd golang-grpc-template
$ go generate ./...
$ go install
```

### From binaries

Download the pre-compiled binaries from the [release page](https://github.com/thazelart/golang-grpc-template/releases) page and copy them to the desired location.

```bash
$ wget https://github.com/thazelart/golang-grpc-template/releases/download/vX.Y.Z/golang-grpc-template_Linux_x86_64.tar.gz
$ tar xvf golang-grpc-template_Linux_x86_64.tar.gz
$ mv golang-grpc-template /usr/local/bin
```

## Generate and use the autocompletion script

```bash
$ golang-grpc-template completion ${0##*/} > /tmp/completion
$ source /tmp/completion
```
