---
layout: post
title:  "set character-set utf8 in mysql client"
date:   2016-11-01 11:17:00
categories: tech 
---

**To see the values of the character set and collation system variables
that apply to your connection, use these statements:**

```sh
show variables like 'character_set%';

show varialbes like 'collation%';
```
upon commend results like this:

```mysql
+--------------------------+----------------------------+
| Variable_name            | Value                      |
+--------------------------+----------------------------+
| character_set_client     | latin1                     |
| character_set_connection | latin1                     |
| character_set_database   | utf8                       |
| character_set_filesystem | binary                     |
| character_set_results    | latin1                     |
| character_set_server     | latin1                     |
| character_set_system     | utf8                       |
| character_sets_dir       | /usr/share/mysql/charsets/ |
+--------------------------+----------------------------+
```
