---
title: "Template"
linkTitle: "Template"
weight: 35
description: >
  Reference for yaml keys that can used for a template.
---

## Defaults

n/a

## Key Appendix

| Key | Required | Explanation |
|---|---|
| `name` | Y | name of the template. |
| `source` | Y | path of the template including source address. (i.e. github.com/github/octocat/.vela/template.yml) |
| `type` | Y | used to look up where to pull the template. |

#### Type Options

* `github` - templates can be stored in any public or private GitHub repository.
