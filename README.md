# CloudEvents Conformance Testing

`cloudevents` is a tool for testing CloudEvents receivers.

[![GoDoc](https://godoc.org/github.com/cloudevents/conformance?status.svg)](https://godoc.org/github.com/cloudevents/conformance)
[![Go Report Card](https://goreportcard.com/badge/cloudevents/conformance)](https://goreportcard.com/report/cloudevents/conformance)

_Work in progress._

## Installation

`cloudevents` can be installed via:

```shell
go get github.com/cloudevents/conformance/cmd/cloudevents
```

To update your installation:

```shell
go get -u github.com/cloudevents/conformance/cmd/cloudevents
```

## Usage

`cloudevents` has two commands at the moment: `invoke` and `listen`. 

### Invoke 

`invoke` will read yaml files, convert them to http and send them to the given target.  

```shell
cloudevents invoke http://localhost:8080 -f ./yaml/v0.3
```

### Listen

`listen` will accept http request and write the converted yaml to stdout.  

```shell
cloudevents listen -v > got.yaml
```

Optionally, you can forward the incoming request to a target.

```shell
cloudevents listen -v -t http://localhost:8181 > got.yaml
```
