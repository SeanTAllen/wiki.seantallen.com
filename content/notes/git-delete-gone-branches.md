---
title: "Delete local branches without a remote"
slug: "git-delete-local-branches-with-gone-remote"
date: 2018-01-05T21:53:25-04:00
draft: false
tags: [Git]
description: "How to change the url for a Git remote."
---
This will delete references to branches that don't exist on the remote:

```bash
git remote prune origin
```

Amusingly, this will not delete all local branches without a remote, because "git". This script will delete all local branches where the remote is "gone":

```bash
git branch -D $(git for-each-ref --format='%(if:equals=[gone])%(upstream:track)%(then)%(refname:short)%(end)' refs/heads)
```

Between the two, that should get everything.

The status of branches can be seen with:

```bash
git branch -v
```
