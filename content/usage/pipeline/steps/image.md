---
title:  "Image"
toc:  true
weight:  1
description: >
  Determine what image the step will run.
---

The `image` declaration for a build step instructs Vela which [Docker image](https://docs.docker.com/engine/docker-overview/#images) to use to create the ephemeral container.
This means setup and install for repository dependencies on the host machine is not required as it ensures all dependencies are available within the image.

```diff
version: "1"

steps:
  - name: test
+   image: golang
    commands:
      - go test ./...

  - name: build
+   image: golang
    commands:
      - go build
```

### Valid Images

Any valid Docker image in any Docker registry can be used for the build environment.

```yaml
image: golang
image: golang:latest
image: golang:1.13
image: library/golang:1.13
image: index.docker.io/library/golang
image: index.docker.io/library/golang:1.13
```

### Pull

Vela will always attempt to pull from its existing cache for images. However, users can force automatic upgrades to images when updates are available.

```diff
version: "1"

steps:
  - name: test
    image: golang
+   pull: true
    commands:
      - go test ./...

  - name: build
    image: golang
+   pull: true
    commands:
      - go build
```
