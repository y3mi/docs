+++
title = "Enabling a Repository"
toc = true
weight = 15
+++

Users will need `admin` access to the GitHub repository to be able to enable the repo in Vela. This is because admin access is required to add webhooks to a repository in GitHub.

To enable a repository execute the following command:

```sh
# Syntax
vela add repo --org <name_of_org> --repo <name_of_repo>

# Example
vela add repo --org github --repo hello-world

repo "github/hello-world" was created
```

This allows Vela to not only trigger builds off opened PRs, but to trigger off any commit to any branch for the repository. Now all that is needed is a [valid Vela configuration file](/usage/reference/cli/authentication) to trigger builds.

_To see all CLI examples for `repo` commands navigate to the [reference section](/usage/reference/cli/repo)._
