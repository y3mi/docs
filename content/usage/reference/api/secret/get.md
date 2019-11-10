---
title: "Get"
linkTitle: "Get"
weight: 10
description: >
  Learn how to  get secrets.
---

## Endpoint

```
GET /api/v1/secrets/:engine/:type/:org/:name
```

| Param | Description |
|---|---|
| engine | Name of a engine. |
| type | Name of the type. |
| org | Name of a organtization. |
| name | Name of a repository or team. |

## Permissions

Documentation Coming Soon!

## Response codes

| Status Code | Description |
|---|---|
| 200 | Indicates the request has succeeded. |
| 401 | Indicates the user does not have proper permissions. |

## Example Response Body

```json
[
	{
		"id": 1,
		"org": "github",
		"repo": "octocat",
		"team": "",
		"name": "foo",
		"value": "",
		"type": "repo",
		"images": [
			"alpine"
		],
		"events": [
			"push"
		]
	},
	{
		"id": 2,
		"org": "github",
		"repo": "*",
		"team": "",
		"name": "foo",
		"value": "",
		"type": "org",
		"images": [
			"alpine"
		],
		"events": [
			"push"
		]
	},
	{
		"id": 3,
		"org": "github",
		"repo": "",
		"team": "octokitties",
		"name": "foo",
		"value": "",
		"type": "shared",
		"images": [
			"alpine"
		],
		"events": [
			"push"
		]
	}
]
```
