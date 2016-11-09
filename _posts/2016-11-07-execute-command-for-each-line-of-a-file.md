---
layout: post
title:  "run command for each line of a txt"
date:   2016-11-07 17:22:00
categories: climbing
---

while read in; do sudo -u apache php occ files:scan "$in"; done < names.txt
