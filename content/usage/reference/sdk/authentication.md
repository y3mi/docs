---
title: "Authentication"
linkTitle: "Authentication"
weight: 10
description: >
  Learn how to authentication.
---

Vela client requires the following four parameters specified to connect to a server.

| Parameter  | Description|
| :---         |     :---     |
| baseURL   | URL to a Vela service.   |
| token | Token is the API key to your account. |


```go
package main

import (
    "github.com/vela/go-vela/vela"

    "fmt"
)

func main() {
    // url is the location of the API server you're trying to hit
    url := "http://localhost:8080"
    token := "qwerty123"
    client, _ := vela.NewClient(url, nil)

    // Use a personal access token that can be generated on
    // the server endpoint /login
    client.Authentication.SetTokenAuth(token)
}
```
