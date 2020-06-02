---
title: "Run GDB in a loop until hitting an error"
slug: "gdb-loop-until-error"
date: 2020-06-02T00:00:25-04:00
draft: false
tags: [GDB]
description: "How to automate multiple `run` commands in GDB."
---
So you have a bug that only happens sometimes and you need to inspect it in GDB? One way to do it would be to start the program then manually do `run` each time it ends until you hit the error.

Better yet, have run executed each time for you on exit until you hit the error.

Here's how:

- Start your program in GDB as you normally would
- Enter the following "magic incantation":

```gdb
set pagination off
b _exit
commands
run
end
```

- Type `run` and enter to start the first run
