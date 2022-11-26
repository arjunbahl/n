---
title: "Important Points | Wordpress Installation"
date: "2017-04-22"
categories: 
  - "research"
---

1. Many a time if wordpress is not given adequate permissions and ownership('www-data') it will guide you tot use SSH2/FTP methods.
2. Also check out https://www.smashingmagazine.com/2014/05/proper-wordpress-filesystem-permissions-ownerships/ for right permissions.
3. Edit the Url in settings in wp-admin, else if you access out of the network it will always "redirect/301" to internal ip which will not be found obviously externally.
