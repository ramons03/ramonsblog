title: LDAP
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-17 12:51:32
tags:
---
https://github.com/osixia/docker-phpLDAPadmin

https://github.com/rroemhild/docker-test-openldap

https://github.com/django-ldapdb/django-ldapdb


docker run -p 6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12


docker run --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12
docker run -p 6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2,PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12


docker run -p 6443:443 \
       --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 \
       --detach osixia/phpldapadmin:0.6.12


docker run -p 6443:443 env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --hostname 192.168.0.114 --detach osixia/phpldapadmin:0.6.12


docker run -p 6443:443,6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12

docker run -p 6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12

http://pissedoffadmins.com/nagios/nagios-error-could-not-stat-command-file-usrlocalnagiosvarrwnagios-cmd.html