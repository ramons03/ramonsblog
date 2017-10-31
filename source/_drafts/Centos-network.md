title: Centos network
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-16 22:00:57
tags:
---
enable epel repo
yum install epel-release -y


nmcli
nmtui


http://www.serverlab.ca/tutorials/linux/administration-linux/configure-centos-6-network-settings/

1.5. NETWORK CONFIGURATION USING A TEXT USER INTERFACE (NMTUI)

The NetworkManager text user interface (TUI) tool, nmtui, provides a text interface to configure networking by controlling NetworkManager. The tool is contained in the subpackage NetworkManager-tui. At time of writing, it is not installed along with NetworkManager by default. To install NetworkManager-tui, issue the following command as root:
~]# yum install NetworkManager-tui
If required, for details on how to verify that NetworkManager is running, see Section 1.4.1, “The NetworkManager Daemon”.
To start nmtui, issue a command as follows:
~]$ nmtui

https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Networking_Guide/ch-Introduction_to_RHEL_Networking.html


iftop 