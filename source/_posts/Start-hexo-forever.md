---
title: Start hexo forever
tags:
  - commands
  - CLI
  - cron
  - linux
categories:
  - Admin
date: 2017-09-15 10:25:00
---

[Forever](https://github.com/foreverjs/forever) is a simple CLI tool for ensuring that a given script runs continuously (i.e. forever).  

```sh
cd location_of_blog_conf_hexo
forever start --uid blog --append -c 'hexo server -p 6000' ./
```
Create a cron to handle restart
```sh
$ crontab -u root -e
@reboot sudo /usr/local/bin/forever start --uid blog --append -c 'hexo server -p 6000 --cwd /pathtoblog' /pathtoblog
```