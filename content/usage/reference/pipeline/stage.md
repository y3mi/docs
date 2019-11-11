---
title: "Stage"
linkTitle: "Stage"
weight: 30
description: >
  Reference for yaml keys that can used for a stage.
---

## Defaults

The `needs` field has a default value set to `clone`. This is because Vela assumes that the stage can't be executed until the workspace is cloned to the agent.

## Key Appendix

| Key | Required | Explanation |
|---|---|
| `name` | Y | name of the build step |
| `needs` | N | stages that must complete before running the current stage (default: `clone`)|
| `steps` | Y | sequential build execution instructions for the stage |
