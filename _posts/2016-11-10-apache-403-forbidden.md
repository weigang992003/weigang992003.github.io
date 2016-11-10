---
layout: post
title:  "apache 403 forbidden error"
date:   2016-11-10 13:44:00
categories: tech
---

vim extra/httpd-vhosts.conf

```sh
<VirtualHost peabox.com:80>
    ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "/Users/fred/workspace/owncloudee"
    ServerName peabox.com
    ErrorLog "/Users/fred/workspace/owncloudee/php.log"
    CustomLog "/private/var/log/apache2/dummy-host2.example.com-access_log" common
    <Directory "/Users/fred/workspace/owncloudee">
       Order allow,deny
       Allow from all
       # New directive needed in Apache 2.4.3:.
       Require all granted
    </Directory>
</VirtualHost>
```
