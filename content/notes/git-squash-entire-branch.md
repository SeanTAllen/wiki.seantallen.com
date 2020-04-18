---
title: "Squash entire git branch"
slug: "squash-git-branch"
date: 2020-04-17T23:00:25-04:00
draft: false
tags: [Git]
description: "Turn all commits on a branch into one commit"
---

You've done a lot of work on a branch and now want to turn the various commits into a single clean commit for merging. GitHub provides an option to do this as "squash and merge". You can use git rebase to select a number of commits and their comments and merge them together.

If you don't care about keeping any comments from the previous commits then resetting your branch from the point the branch was created, staging them, and then committing.

To set if you are using `bash`:

```bash
git reset $(git merge-base master $(git rev-parse --abbrev-ref HEAD))
```

To reset if you are using `fish`:

```fish
git reset (git merge-base master (git rev-parse --abbrev-ref HEAD))
```

After resetting you can then do:

```bash
git add .
git commit
```
