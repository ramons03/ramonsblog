title: mount disk centos
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-09-24 21:59:57
tags:
---
https://www.centos.org/forums/viewtopic.php?t=29878

Found the problem - missing packages (nfs-utils, nfs4-acl-tools, portmap) Seems to work OK with quick tests.

sda disco principal
sdb discos secundarios

fsdisk -l /dev/sdb


mount -t ext4 /dev/sdb1 mnt/disk1