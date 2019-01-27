---
title: "Login to Docker container"
slug: "login-to-docker-container"
date: 2019-01-27T21:53:25-04:00
draft: false
tags: [Docker]
description: "How to get a shell in a Docker container so you can run commands and otherwise test/get things working."
---
```bash
docker run --name LOCAL_NAME_FOR_IMAGE --user USER_TO_LOGIN_AS --rm -i -t DOCKER_IMAGE_URL bash
```

For example:

```bash
docker run --name ponyc-ci-llvm-391 --user pony --rm -i -t ponylang/ponyc-ci:llvm-3.9.1 bash
```