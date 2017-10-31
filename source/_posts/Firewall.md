title: Firewall. Open port for CentOS 7
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-08-01 00:42:56
tags:
---
### Commands

  ```sh
  systemctl status firewalld
  firewall-cmd --state
  firewall-cmd --get-services
  firewall-cmd --info-service=service-name
  ls /usr/lib/firewalld/services/
  firewall-cmd --zone=public --permanent --add-port=8080/tcp
  firewall-cmd --reload
  ```
  
Use this command to find your active zone(s):
```sh
firewall-cmd –get-active-zones
```
It will say either public, dmz, or something else. You should only apply to the zones required.

In the case of dmz try:
```sh
firewall-cmd –zone=dmz –add-port=2888/tcp –permanent
```
Otherwise, substitute dmz for your zone, for example, if your zone is public:
```sh
firewall-cmd –zone=public –add-port=2888/tcp –permanent
```
Then remember to reload the firewall for changes to take effect.
```sh
firewall-cmd –reload
```

  
  
  [Documentation](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Security_Guide/sec-Using_Firewalls.html)