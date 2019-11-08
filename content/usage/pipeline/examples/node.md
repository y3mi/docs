---
title: "Node"
toc: true
weight: 3
description: >
  Sample Node Pipeline
---

```yaml
version: "1"

steps:
  - name: install
    image: node:latest
    pull: true
    commands:
      - yarn

  - name: lint
    image: node:latest
    pull: true
    commands:
      - yarn lint

  - name: build
    image: node:latest
    pull: true
    commands:
      - yarn build
```
