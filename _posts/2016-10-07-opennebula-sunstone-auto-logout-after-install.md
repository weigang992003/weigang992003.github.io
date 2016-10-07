---
layout: post
title:  "opennebula auto logout after install"
date:   2016-10-07 21:49:00
categories: learning
---

# opennebula auto logout after install

I install opennebula on centos7 within virtualbox, after I login the system it auto logout. Then i found time on centos is not correct, so the cookie time is not accord with the server. So run the following command to correct centos time.

>> ntpdate 0.asia.pool.ntp.org