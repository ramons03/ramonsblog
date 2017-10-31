title: docker phpldapadmin
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-09-16 10:38:14
tags:
---
```sh
docker pull rroemhild/test-openldap
docker run --privileged -d -p 389:389 rroemhild/test-openldap


git clone https://github.com/ramons03/djangoldapsample.git


python manage.py runserver

docker run --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12
docker run -p 6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2,PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12


docker run -p 6443:443 \
       --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 \
       --detach osixia/phpldapadmin:0.6.12


docker run -p 6443:443 env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --hostname 192.168.0.114 --detach osixia/phpldapadmin:0.6.12


docker run -p 6443:443,6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12

docker run -p 6800:80 --env PHPLDAPADMIN_LDAP_HOSTS=172.17.0.2 --env PHPLDAPADMIN_HTTPS=false --detach osixia/phpldapadmin:0.6.12
```

http://pissedoffadmins.com/nagios/nagios-error-could-not-stat-command-file-usrlocalnagiosvarrwnagios-cmd.html