+++
title = "Roles"
toc = true
weight = 10
+++

Vela does not maintain any authentication (AuthN) and authorization (AuthZ) internally but instead, inherits it access from the source (version control) provider. Currently, Vela can connect to a GitHub instance, so it uses [GitHub's access model](https://help.github.com/en/articles/access-permissions-on-github) for access control.

* Admin
* Write
* Read

Admins within the GitHub organization have the option to use GitHub orgs to allow users to have permissions on all repositories in the org, or to use fine grained access of adding access for users directly to individual repositories.

### Admin

The **admin** role enables full access to the repository which grants the following access levels for resources:

* Build: Read/Write
* Log: Read/Write
* Repository: Read/Write
* Secret: Read/Write
* Step: Read/Write

### Write

The **write** role enables read and write access to the repository which grants the following access levels for resources:

* Build: Read/Write
* Log: Read/Write
* Repository: Read
* Secret: None
* Step: Read/Write

### Read

The **read** role enables read access to the repository which grants the following access levels for resources:

* Build: Read
* Log: Read
* Repository: Read
* Secret: None
* Step: Read
