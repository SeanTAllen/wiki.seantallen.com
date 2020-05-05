---
title: "Build a new Docker container"
slug: "build-a-new-docker-container"
date: 2019-01-27T00:00:25-04:00
draft: false
tags: [Docker]
description: "How to build a new Docker container."
---
```bash
docker build -t URL_FOR_CONTAINER .
```

For example:

```bash
docker build -t ponylang/ponyc-ci:llvm-3.9.1 .
```

To use a Dockerfile other than `Dockerfile` in the local directory:

```bash
docker build -t ponylang/ponyc-ci:llvm-3.9.1 --file Dockerfile.llvm391 .
```
