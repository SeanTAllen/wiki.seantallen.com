---
title: "Update Git repo from remote"
slug: "git-fork-update"
date: 2020-04-17T12:53:25-04:00
draft: false
tags: [Git]
description: "Update a Git repo with content from a remote"
---

The most common use case for this would be to sync a forked GitHub repo with the repo you forked it from. It is also the same process you would use in a non-Github workflow to keep your repo up-to-date with all the changes in a remote.

The example below assumes that you, want to:

- Name the remote "upstream"
- Want to update your master branch to match the remote's master branch

```bash
# Add the remote, call it "upstream":

git remote add upstream https://github.com/whoever/whatever.git

# Fetch all the branches of that remote into remote-tracking branches,
# such as upstream/master:

git fetch upstream

# Make sure that you're on your master branch:

git checkout master

# Rewrite your master branch so that any commits of yours that
# aren't already in upstream/master are replayed on top of that
# other branch:

git rebase upstream/master
```
