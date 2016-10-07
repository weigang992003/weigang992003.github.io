---
layout: post
title:  "Can not get on web UI remotely(Centos 7 and opennebula 5.0.2)"
date:   2016-10-07 21:39:00
categories: learning
---

# Can not get on web UI remotely(Centos 7 and opennebula 5.0.2)

CentOS 7 uses the firewalld service for its firewall (although iptables can still be used to list firewall info). These commands should permanently open port 9869:

>> firewall-cmd --zone=public --add-port=9869/tcp --permanent
>> firewall-cmd --reload


