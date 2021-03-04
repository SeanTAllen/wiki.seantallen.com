---
title: "Set WSL default user"
slug: "wsl-default-user"
date: 2021-03-03T21:00:42-04:00
draft: false
tags: [WSL]
description: "Set the default user for a WSL distribution in the Windows registry."
---

Navigate in Registry Editor to the list of distributions installed.

```text
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Lxss
```

You'll see a listing of UUIDs for each installed distribution. You can tell which is which, by checking their `DistributionName` key. Once you find the distribution you want, set the `DefaultUid` to the user id for the user that should be the default when starting up the distribution.

It's important to set a default user as this is the user that VSCode will use if you start up VSCode from inside WSL.

Alternately, you can set the user in `/etc/wsl.conf` for the given distribution:

```toml
[user]
default=sean
```
