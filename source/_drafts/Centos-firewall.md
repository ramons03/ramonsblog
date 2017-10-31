title: Centos firewall
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-17 00:13:07
tags:
---
Use this command to find your active zone(s):

firewall-cmd --get-active-zones
It will say either public, dmz, or something else. You should only apply to the zones required.

In the case of dmz try:

firewall-cmd --zone=dmz --add-port=2888/tcp --permanent
Otherwise, substitute dmz for your zone, for example, if your zone is public:

firewall-cmd --zone=public --add-port=2888/tcp --permanent
Then remember to reload the firewall for changes to take effect.

firewall-cmd --reload


open port 80
doble --

firewall-cmd –zone=dmz –add-port=2888/tcp –permanent
Otherwise, substitute dmz for your zone, for example, if your zone is public:

firewall-cmd -–zone=public –add-port=2888/tcp –permanent
Then remember to reload the firewall for changes to take effect.

firewall-cmd –reload