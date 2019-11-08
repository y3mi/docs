+++
title = "Viewing Builds"
toc = true
weight = 20
+++

### Get list of builds

To get a list of builds for a repository execute the following command:

```sh
# Syntax
vela get build --org <name_of_org> --repo <name_of_repo>

# Example
vela get build --org github --repo hello-world

NUMBER  STATUS  EVENT   AUTHOR
1       success push    Octocat
2       failed  push    Octocat
3       pending push    Octocat
```

### View build details

To view the details for a build execute the following command:

```sh
# Syntax
vela view build --org <name_of_org> --repo <name_of_repo> --build-number <build_number>

# Example
vela view build --org github --repo hello-world --build-number 1

id: 1
repositoryid: 1
number: 1
parent: 1
event: push
status: pending
error: ""
enqueued: 1556730001
created: 1556720958
started: 1556730001
finished: 1556730045
deploy: ""
clone: https://github.com/github/hello-world.git
source: https://github.com/github/hello-world/commit/7fd1a60b01f91b314f5995aa4e4d4e80d8edf11d
title: Merge pull request #6 from Octocat/patch-1
message: |-
  Merge pull request #6 from Octocat/patch-1
  New line at end of file.
commit: 7fd1a60b01f91b314f5995aa4e4d4e80d8edf11d
sender: Octocat
author: Octocat
branch: master
ref: refs/heads/master
baseref: ""
```

_To see all CLI examples for `build` commands navigate to the [reference section](/usage/reference/cli/build)._
