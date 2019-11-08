---
title: "Go"
toc: true
weight: 1
description: >
  Sample Go Pipeline
---

```yaml
version: "1"

steps:
  - name: install
    image: golang:latest
    pull: true
    environment:
      CGO_ENABLED: '0'
      GOOS: linux
    commands:
      - go get ./...

  - name: test
    image: golang:latest
    pull: true
    environment:
      CGO_ENABLED: '0'
      GOOS: linux
    commands:
      - go test ./...

  - name: build
    image: golang:latest
    pull: true
    environment:
      CGO_ENABLED: '0'
      GOOS: linux
    commands:
      - go build
```
