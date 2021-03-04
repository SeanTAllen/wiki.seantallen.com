---
title: "Restart a CircleCI job without SSH"
slug: "restart-circleci-without-ssh"
date: 2019-04-03T00:00:25-04:00
draft: true
tags: [CircleCI]
description: "How to restart a CircleCI job without using SSH session."
---

So, CircleCI has the ability to restart failed jobs. Most of the time there is a rerun button (or so I remember), but sometimes there isn't. I have no idea why. There is an option to return with an SSH session. That works, but the job will continue for 10 minutes before counting as passing until the SSH session times out as inactive. You can however visit a URL and trigger a new build without using the SSH session option.

```
https://circleci.com/actions/retry/github/USERNAME/REPO/TEST_NUMBER
```

for example:

```
https://circleci.com/actions/retry/github/wallaroolabs/wallaroo/17971
```
