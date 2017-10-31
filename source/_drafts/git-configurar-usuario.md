title: git configurar usuario
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-17 00:30:09
tags:
---
Ignore that git is configuring your email and because, is not happening because your are not signed in at the moment that you clone your repository. Or your global configuration is empty

So reconfigure your email and name

   
 git config --global user.name "Your Name" 
git config --global user.email you@example.com
Then add a commit message and run

git commit --amend --reset-author
of course push again