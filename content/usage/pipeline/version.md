---
title:  "Version"
toc:  true
weight:  2
description: >
  Set the Vela YAML version.
---

The `version` declaration instructs Vela of the configuration syntax for the pipeline and the functionality being utilized within the pipeline.

```diff
+metadata
+  version: "1"

steps:
  - name: test
    image: golang
    commands:
      - go test ./...

  - name: build
    image: golang
    commands:
      - go build
```
