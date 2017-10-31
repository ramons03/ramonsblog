title: Apache VirtualHost
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-15 14:54:48
tags:
---



Setup a Virtual Domain
```xml
NameVirtualHost *
<VirtualHost *>
  DocumentRoot /web/example.com/www
  ServerName www.example.com
  ServerAlias example.com
  CustomLog /web/example.com/logs/access.log combined
  ErrorLog /web/example.com/logs/error.log
</VirtualHost>
```


Setup a proxy
```xml
NameVirtualHost *
<VirtualHost *>
  DocumentRoot /web/example.com/www
  ServerName www.example.com
  ServerAlias example.com
  CustomLog /web/example.com/logs/access.log combined
  ErrorLog /web/example.com/logs/error.log
</VirtualHost>
```

Include another conf file

Include /etc/apache/virtual-hosts/*.conf


Hide apache version info

ServerSignature Off
ServerTokens Prod


Custom 404 Error message


ErrorDocument 404 /404.html


Create a virtual directory (mod_alias)


Alias /common /web/common


Perminant redirect (mod_alias)


Redirect permanent /old http://example.com/new


Create a cgi-bin


ScriptAlias /cgi-bin/ /web/cgi-bin/


Process .cgi scripts


AddHandler cgi-script .cgi


Add a directory index


DirectoryIndex index.cfm index.cfm


Turn off directory browsing


Options -Indexes


Turn on directory browsing


<Location /images>
  Options +Indexes
</Location>


Create a new user for basic auth (command line)


htpasswd -c /etc/apacheusers


Apache basic authentication


AuthName "Authentication Required"
AuthType Basic
AuthUserFile /etc/apacheusers
Require valid-user

Only allow access from a specific IP

Order Deny,Allow
Deny from all
Allow from 127.0.0.1

Only allow access from your subnet

Order Deny,Allow
Deny from all
Allow from 176.16.0.0/16

mod_rewrite

Turn on the rewrite engine

RewriteEngine On

Redirect /news/123 to /news.cfm?id=123

RewriteRule ^/news/([0-9]+)$ /news.cfm?id=$1 [PT,L]

Redirect www.example.com to example.com

RewriteCond %{HTTP_HOST} ^www\.example\.com$ [NC]
RewriteRule ^(.*)$ http://example.com$1 [R=301,L]
      ```sh
      sudo rpm --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro
      sudo rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm
       ```