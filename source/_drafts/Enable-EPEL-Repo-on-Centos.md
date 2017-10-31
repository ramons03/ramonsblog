title: Enable EPEL Repo on Centos
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-17 20:17:31
tags:
---
What is the EPEL repo?

The EPEL (Extra Packages for Enterprise Linux) yum repository is an excellent source for additional packages for CentOS. Instead of having to compile applications that aren’t included in CentOS’ built-in repositories from source, EPEL can be used.

Install/enable the EPEL repo:

1
yum install epel-release -y
 Disable the EPEL repo:

Open /etc/yum.repos.d/epel.repo and set any instance of ‘enabled=1’ to ‘enabled=0’

 

Old Instructions

These are old instructions for installing the EPEL repository RPM. Use this if the above process does not work for you.

The EPEL repo is enabled by simply installing an RPM. Please use the command below to install the EPEL repository on your CentOS server. If you are unsure of your CentOS version or architecture, please click here to find your server’s CentOS version and architecture.

CentOS 6 – 32-bit

1
rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
 CentOS 6 – 64-bit

1
rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
 CentOS 5 – 32-bit

1
rpm -Uvh http://dl.fedoraproject.org/pub/epel/5/i386/epel-release-5-4.noarch.rpm
 CentOS 5 – 64-bit

1
rpm -Uvh http://dl.fedoraproject.org/pub/epel/5/x86_64/epel-release-5-4.noarch.rpm
After running the above commands for your relevant CentOS version, the following file is created:

/etc/yum.repos.d/epel.repo
The above file can be edited directly to enable or disable the EPEL repo.