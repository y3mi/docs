---
title: "View"
linkTitle: "View"
weight: 15
description: >
  Learn how to  view a step.
---

## Endpoint

```
GET /api/v1/repos/:org/:repo/builds/:build/steps/:step
```

| Param | Description |
|---|---|
| org | Name of a organtization. |
| repo | Name of a repository. |
| build | Number of build. |
| step | Number of step. |

## Permissions

Documentation Coming Soon!

## Response codes

| Status Code | Description |
|---|---|
| 200 | Indicates the request has succeeded. |
| 401 | Indicates the user does not have proper permissions. |

## Example Response Body

```json
{
	"id": 1,
	"build_id": 1,
	"repo_id": 1,
	"number": 1,
	"name": "clone",
	"status": "success",
	"error": "",
	"exit_code": 0,
	"created": 1563475419,
	"started": 0,
	"finished": 0,
	"host": "host.company.com",
	"runtime": "docker",
	"distribution": "linux"
}
```
