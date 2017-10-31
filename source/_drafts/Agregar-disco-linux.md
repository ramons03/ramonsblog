title: Agregar disco linux
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-09-22 07:41:12
tags:
---
http://www.yolinux.com/TUTORIALS/LinuxTutorialAdditionalHardDrive.html

[root]# fdisk /dev/sdb
Command (m for help): m     (Enter the letter "m" to get list of commands)
Command action
   a   toggle a bootable flag
   b   edit bsd disklabel
   c   toggle the dos compatibility flag
   d   delete a partition
   l   list known partition types
   m   print this menu
   n   add a new partition
   o   create a new empty DOS partition table
   p   print the partition table
   q   quit without saving changes
   s   create a new empty Sun disklabel
   t   change a partition's system id
   u   change display/entry units
   v   verify the partition table
   w   write table to disk and exit
   x   extra functionality (experts only)

Command (m for help): n
Command action
   e   extended
   p   primary partition (1-4)
p
Partition number (1-4): 1
First cylinder (1-9729, default 1):
Using default value 1
Last cylinder, +cylinders or +size{K,M,G} (1-9729, default 9729):
Using default value 9729

Command (m for help): w    (Write and save partition table)

[root]# mkfs.ext4 -L disk2 /dev/sdb1




	
How come we have many ways to do this but as always we also take into consideration and do not know where the file system used in the device may hinder a little, but we can use the "auto" option to give a little help.

mount -t auto /dev/sdb1 /media/pendrv
and ready our device will be mounted: at /media/pendrv ready to use, then simply use:

umount /media/pendrv