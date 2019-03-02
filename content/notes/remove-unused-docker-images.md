title: "Remove unused Docker images"
slug: "remove-unused-docker-images"
date: 2019-02-28T00:00:25-04:00
draft: false
tags: [Docker]
description: "How to clear up space by removing unused Docker images."
---

```bash
docker images -q | xargs docker rmi
```