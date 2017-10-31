title: Bug on Git Jul 2017
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-08-18 10:32:35
tags:
---
### You must update git to last version  

[Update details](https://github.com/git/git/commit/820d7650cc670d3e4195aad3a5343158c316e8fa)

```
connect: reject ssh hostname that begins with a dash
When commands like "git fetch" talk with ssh://$rest_of_URL/, the
code splits $rest_of_URL into components like host, port, etc., and
then spawns the underlying "ssh" program by formulating argv[] array
that has:

 - the path to ssh command taken from GIT_SSH_COMMAND, etc.

 - dashed options like '-batch' (for Tortoise), '-p <port>' as
   needed.

 - ssh_host, which is supposed to be the hostname parsed out of
   $rest_of_URL.

 - then the command to be run on the other side, e.g. git
   upload-pack.

If the ssh_host ends up getting '-<anything>', the argv[] that is
used to spawn the command becomes something like:

    { "ssh", "-p", "22", "-<anything>", "command", "to", "run", NULL }

which obviously is bogus, but depending on the actual value of
"<anything>", will make "ssh" parse and use it as an option.

Prevent this by forbidding ssh_host that begins with a "-".

Noticed-by: Joern Schneeweisz of Recurity Labs
Reported-by: Brian at GitLab
Signed-off-by: Junio C Hamano <gitster@pobox.com>
Reviewed-by: Jeff King <peff@peff.net>
Signed-off-by: Junio C Hamano <gitster@pobox.com>
```

[Como actualizar git en centos](https://stackoverflow.com/questions/21820715/how-to-install-latest-version-of-git-on-centos-6-x-7-x):
```
yum install http://opensource.wandisco.com/centos/6/git/x86_64/wandisco-git-release-6-1.noarch.rpm
yum install git
git --version
```