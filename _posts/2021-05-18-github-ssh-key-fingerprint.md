---
title: GitHub ssh key fingerprint
layout: post
date: 2021-05-18 13:26:00 +0200
tags: [ssh, git, github, cli]
---
Github shows a hash when you add an ssh key. This can be cross-checked with the cli.

To check whether you have the key in your agent:

```sh
ssh-add -l -E md5
```

To check whether you have the key at all that matches the fingerprint:

```sh
find ~/.ssh -name '*.pub' | xargs -n1 ssh-keygen -l -E md5 -f
```
