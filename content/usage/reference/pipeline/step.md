---
title: "Step"
linkTitle: "Step"
weight: 25
description: >
  Reference for yaml keys that can used for a step.
---

## Defaults

n/a

## Key Appendix

| Key | Required | Explanation |
|---|---|---|
| `commands` | N | specifiy the commands to be run inside step |
| `detach` | N | specifiy if the container should detach as a service |
| `entrypoint` | N | overwrite default container executable  |
| `environment` | N | environment varibles to be added at runtime |
| `image` | Y | name of the Docker image |
| `name` | Y | name of the step |
| `parameters` | N | variables under key are injected with `PARAMETER_`  |
| `privileged` | N | specifiy if the container should run with privileges |
| `pull` | N | specifiy if the container image should be pulled before build |
| `ruleset` | N | set of rules to decide when step should run |
| `secrets` | N | set of secrets to be injected as all uppercase environment variables |
| `template` | N | when set expands template into step  |
| `ulimit` | N | set ulimit values for syscall (Requries `privileged: true`) |
| `volume` | N | specify a volume to store data |
