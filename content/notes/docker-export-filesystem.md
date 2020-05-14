---
title: "Export Docker Filesystem"
slug: "docker-export-filesystem"
date: 2020-05-14T12:43:15-04:00
tags: [Docker]
description: "How to export the filesystem from a Docker image to a .tar."
---

```bash
docker run --name TO_EXPORT -it -d TAG
docker export --output FILE_NAME.tar TO_EXPORT
docker stop TO_EXPORT
docker rm TO_EXPORT
```

for example:

```bash
docker run --name wsl-ubuntu-20-daily -it -d seantallen/wsl-ubuntu-20-daily:20200514
docker export --output /mnt/c/Users/sean/wsl-vms/wsl20-base.tar wsl-ubuntu-20-daily
docker stop wsl-ubuntu-20-daily
docker rm wsl-ubuntu-20-daily
```
