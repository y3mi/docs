---
title: "Stage"
linkTitle: "Stage"
weight: 30
description: >
  Reference for yaml keys that can used for a stage.
---

| Key | Explanation |
|---|---|
| `name` | name of the build step |
| `needs` | stages that must complete before running the current stage (default: `clone`)|
| `steps` | sequential build execution instructions for the stage |

## Defaults

The `needs` field has a default value set to `clone`. This is because Vela assumes that the stage can't be executed until the workspace is cloned to the agent.
