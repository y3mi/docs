---
title: "Service"
linkTitle: "Service"
weight: 20
description: >
  Reference for yaml keys that can used for a service.
---

## Defaults

n/a

## Key Appendix

| Key | Required | Explanation |
|---|---|
| `entrypoint` | N | overwrite default container executable  |
| `environment` | N | environment varibles to be added at runtime |
| `image` | Y | name of the Docker image |
| `name` | Y | name of the service |
| `ports` | N | specifiy the port container will listen on |
