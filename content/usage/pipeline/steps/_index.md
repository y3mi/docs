---
title:  "Steps"
toc:  true
weight:  4
description: >
  Execute a build step.
---

Steps run inside a Docker image and contain the information required to execute a command (or commands) specified by the user.

All steps begin with a `name: ` field which is used to identify the step. Having multiple steps with the same name can result in some unexpected behaviour.
