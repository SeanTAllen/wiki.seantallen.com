---
title: "Remove a Git submodule"
slug: "remove-git-submodule"
date: 2018-01-05T21:53:25-04:00
draft: false
tags: [Git]
description: "How to delete a Git submodule."
---
This is certainly a lot more involved than one would imagine.

The following assumes that the submodule is `MODULE/TO-REMOVE`:

{{% note %}}
Note: Do not put a trailing slash at the end of `MODULE/TO-REMOVE` or you will get errors.
{{% /note %}}

1. Delete the relevant section from `.gitmodules`
2. `git add .gitmodules`
3. Delete the relevant section from `.git/config`
4. `git rm --cached MODULE/TO-REMOVE`
5. `rm -rf .git/modules/MODULE/TO-REMOVE`
6. `rm -rf MODULE/TO-REMOVE`
7. `git add .`
8. `git commit`
9. `git push`

