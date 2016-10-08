---
layout: post
title:  "Install Centos7 in Virtualbox"
date:   2016-10-07 21:39:00
categories: learning
---

# Install Centos7 in Virtualbox

>> set network bridged

## ip config
>> nmtui
>> yum install net-tools


## The following operation all did in local terminal

>> ssh-copy-id -i ~/.ssh/id_rsa.pub root@192.168.31.101  
>> vi /etc/locale.conf  
>> add new line: LC_ALL="en_US.UTF-8"

## ntpdate

yum install ntp //安装ntp服务
systemctl enable ntpd //开机启动服务
systemctl start ntpd //启动服务
timedatectl set-timezone Asia/Shanghai //更改时区
timedatectl set-ntp yes //启用ntp同步
ntpq -p //同步时间

>> yum install lvm2
