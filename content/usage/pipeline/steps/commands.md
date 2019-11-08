---
title: "Commands"
weight: 10
description: >
  List commands the step will execute.
---

The `commands` declaration for a build step instructs Vela what commands to execute inside the container using the local [shell](https://en.wikipedia.org/wiki/Shell_(computing)) environment.

```diff
version: "1"

steps:
  - name: build
    image: golang
+   commands:
+     - go test ./...
+     - go build
```

Using the above example, the provided commands are converted to a simple shell script that looks like:

```sh
#!/bin/sh

set -e

go test ./...

go build
```

In turn, the above shell script is executed as the Docker entrypoint for the container:

```sh
docker run --entrypoint=build.sh golang
```
