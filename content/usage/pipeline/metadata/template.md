---
title:  "Template"
toc:  true
weight:  2
description: >
  Flag if the pipeline is a template or not.
---

```diff
+metadata
+  template: true

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
