---
title: Running bash file with ZSH
author: Dustin Petersen
date: 2019-08-08 14:10:00 +0800
categories: [zsh, bash]
tags: [writing]
---

## I have switched to zsh, how can I run a script which is written for bash?

You can run the script with bash manually:

`bash myscript.sh`

A better and more permanent solution is to add a shebang line:

`#!/usr/bin/env bash`

one that line has been added, you can run it directly from zsh.

` % ./myscript.sh`
