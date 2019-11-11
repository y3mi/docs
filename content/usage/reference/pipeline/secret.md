---
title: "Secret"
linkTitle: "Secret"
weight: 35
description: >
  Reference for yaml keys that can used for a secret.
---

## Defaults

Since the `key`, `engine` and `type` fields have default values set, **these can be skipped** and Vela will implicitly set them.

```diff
version: "1"

steps:
  - name: docker
    image: docker.registry.com/vela-plugins/docker:1
    registry: docker.registry.com
    repo: docker.registry.com/app/hello-world
    secrets: [ docker_username, docker_password ]
    auto_tag: true

secrets:
  - name: docker_username
-   key: docker_username
-   engine: native
-   type: repo
  - name: docker_password
-   key: docker_password
-   engine: native
-   type: repo
```

## Key Appendix

| Key | Value | Explanation |
|---|---|---|
| `engine` | `native` | secret backend the worker uses to lookup the secret (default: `native`) |
| `key` | `docker_username` | key to the secret variable to lookup from the secret backend (default: secret `name`)|
| `name` | `docker_username` | name of the secret variable to be injected into the build |
| `type` | `repository` | secret type the worker uses to lookup the secret (default: `repository`) |

#### Engine Options

* `native` - stores the secret in the Vela database
* `vault` - stores the secret in the Vela Vault namespace

#### Type Options

* `repository` - secrets that can only be used by a single repository
* `organization` - secrets that can be used by any repository in a single organization
* `shared` - secrets that can be used by any repository in any organization
