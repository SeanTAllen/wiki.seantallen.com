 ---
title: "VSCode Makefile handling"
slug: "vscode-makefile-tabs"
date: 2019-02-05T00:00:25-04:00
draft: false
tags: [VSCode]
description: "Automatically use tabs in Makefiles with VSCode"
---

 It's a little fiddly to get it to properly handle Makefiles for tabs/spaces if you normally use spaces for indentation in your projects. The following should be aded into the `settings.json`.

 ```json
    "[makefile]": {
        "editor.tabSize": 2,
        "editor.insertSpaces": false,
        "editor.detectIndentation": false
    },
```
