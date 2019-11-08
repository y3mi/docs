---
title:  "Stages"
toc:  true
weight:  5
description: >
  Execute build steps in parallel.
---

Stages are a grouping of steps. They contain a name and an array of steps.

By default, all stages run in **parallel**.

You can specify that a stage requires another stage's completion by using the `needs:` field. Needs takes an array of stage names that need to be completed before the given step can begin.

```
version: "1"

stages:

  backend:
    steps:
      - name: install
        image: golang:latest
        commands:
          - go get ./...
      - name: test
        image: golang:latest
        commands:
          - go test ./...
      - name: build
        image: golang:latest
        commands:
          - go build

  frontend:
    steps:
      - name: install
        image: npm:latest
        commands:
          - npm install
      - name: test
        image: npm:latest
        commands:
          - npm run test
      - name: build
        image: npm:latest
        commands:
          - npm run build

  notify:
    needs: [ backend, frontend ]
    steps:
      - name: notify
        image: alpine
        commands:
          - echo Completed!
```

In this example, `notify` will only begin once `backend` and `frontend` complete. This allows the backend and frontend steps to complete independently.
