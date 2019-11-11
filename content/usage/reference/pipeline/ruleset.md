---
title: "Ruleset"
linkTitle: "Ruleset"
weight: 35
description: >
  Reference for yaml keys that can used for a rulesets.
---

## Defaults

n/a

## Key Appendix

#### ruleset keys

| Key | Required | Explanation |
|---|---|
| `continue` | N | set `true` to continue steps on failure (Default: `false`)  |
| `if` | N | used in conjunction with rules  |
| `operator` | N | control and/or operator logic with rulesets (Default: `and`) |
| `unless` | N | used in conjunction with rules  |

#### rule keys

_All keys are array types_

| Key | Required | Explanation |
|---|---|
| `branch` | N | name or glob match for branches |
| `event` | N | type of events  |
| `path` | N | files or paths within repo |
| `repo` | N | name or glob match for repositories |
| `status` | N | type of status |
| `tag` | N | name or glob match for tags |

##### event options

* `push` - event type for build and repo push events
* `pull_request` - event type for build and repo pull_request events
* `tag` - event type for build and repo tag events

##### status options

* `failure` - status type for build and step failure statuses
* `killed` - status type for build and step killed statuses
* `success` - status type for build and step success statuses
