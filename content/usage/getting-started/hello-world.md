+++
title = "Hello World"
toc = true
weight = 50
+++

Here's a sample pipeline to build a Go binary.

```yaml
version: "1"

steps:

  # Build the Go binary in the latest Golang Docker image.
  - name: build
    image: golang:latest
    pull: true
    environment:
      CGO_ENABLED: "0"
    commands:
      - go build -o release/my_binary
```
