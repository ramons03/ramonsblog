title: git push
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-09-23 03:57:25
tags:
---
https://stackoverflow.com/questions/24114676/git-error-failed-to-push-some-refs-to

If the GitHub repo has seen new commits pushed to it, while you were working locally, I would advice for:

git pull --rebase
git push
The full syntax is:

git pull --rebase origin master
git push origin master
That way, you would replay (the --rebase part) your local commits on top of the newly updated origin/master (or origin/yourBranch: git pull origin yourBranch).

See a more complete example in the chapter 6 Pull with rebase of the Git Pocket Book.

I would recommend a:

git push -u origin master
That would establish a tracking relationship between your local master branch and its upstream branch.
After that, any future push for that branch can be done with a simple:

git push
See "Why do I need to explicitly push a new branch?".

Since the OP already reset and redone its commit on top of origin/master:

git reset --mixed origin/master
git add .
git commit -m "This is a new commit for what I originally planned to be amended"
git push origin master
There is no need to pull --rebase.

Note: git reset --mixed origin/master can also be written git reset origin/master, since the --mixed option is the default one when using git reset.