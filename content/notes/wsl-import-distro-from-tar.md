---
title: "Import WSL distribution from a tar archive"
slug: "wsl-import-distro-from-tar"
date: 2020-05-14T12:56:38-04:00
draft: false
tags: [WSL]
description: "How to turn a .tar file, like an exported Docker container filesystem, into a WSL distribution."
---
```pwsh
wsl --import MY-DISTRO .\MY-DISTRO-LOCATION\ .\ARCHIVE.tar
```

For example:

```pwsh
wsl --import ubuntu-20-daily .\ubuntu-20-daily\ .\wsl20-base.tar
```
