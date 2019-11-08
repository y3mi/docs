---
title:  "Parameters"
toc:  true
weight:  8
description: >
  Set variables that a plugin will consume.
---

The parameters declaration for a build step is used to pass values to a plugin.

Parameters are injected into the build step as `PARAMETER_[NAME]`

The values needed for a plugin are documented in that plugins docs.

```diff
steps:
  - name: api-call
    image: myplugin:v1.0.0
    pull: true
+   parameters:
+     api_url: 'myapi.mydomain.com'
    commands:
      - go get ./...
```

This would set an environment variable of `PARAMETER_API_URL` with a value of `myapi.mydomain.com`
