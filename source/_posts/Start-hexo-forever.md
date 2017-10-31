title: Start hexo forever
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
tags:
  - commands
  - CLI
categories:
  - Admin
date: 2017-09-15 10:25:00
---
[Forever](https://github.com/foreverjs/forever) is a simple CLI tool for ensuring that a given script runs continuously (i.e. forever).  

```sh
cd location_of_blog_conf_hexo
forever start --uid blog --append -c 'hexo server -p 6000' ./
```