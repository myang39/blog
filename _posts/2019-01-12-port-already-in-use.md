---
layout: post
title:  "handy tricks: find port and kill it"
date:   2019-01-12
categories: jekyll update
author: "Luke"
---

1. 烦人的端口被占用? Port 3000 is already in use 杀掉它
step1:

$ lsof -i tcp:3000
在return一堆东西 找到 PID (process identifier)

step2:

$ kill -9 `${the PID found in step1}` 
