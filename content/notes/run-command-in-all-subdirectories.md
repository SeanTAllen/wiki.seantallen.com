---
title: "Run command in all subdirectories"
slug: "run-command-in-all-subdirectories"
date: 2020-06-02T00:00:25-04:00
draft: false
tags: [shell]
description: "How to automate running a command in all subdirectories."
---
Should work for any shell. Here, the command to be run is a bash command. The `-exec` can be updated to whatever from the example.

```console
find . -maxdepth 1 -type d \( ! -name . \) -exec bash -c "cd '{}' && git pull" \;
```
