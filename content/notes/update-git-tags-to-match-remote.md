---
title: "Update git tags to match remote"
slug: "Update git tags to match remote"
date: 2019-12-18T12:53:25-04:00
draft: false
tags: [Git]
description: "How to 'remove' tags that aren't in the remote"
---

```bash
git tag -l | xargs git tag -d
git fetch --tags
```

The first line deletes all tags in the current repo. The second fetches all tags from our remote.
