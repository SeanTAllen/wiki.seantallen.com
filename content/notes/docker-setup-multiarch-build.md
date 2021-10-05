---
title: "Setup for multi-arch build"
slug: "setup-multiarch-build"
date: 2019-02-28T00:00:25-04:00
draft: false
tags: [Docker]
description: "How to set-up for doing multi-arch build."
---

```bash
docker run --privileged --rm tonistiigi/binfmt --install all
```
