---
title: "Debian Configure Firewall"
date: 10-09-2022 14:00
categories: [Linux]
tags: [linux, install, config, debian, firewall]
---

# Summary
How to configure the Debian firewall UFW

## Requirements
* Debian Linux (lightweight install)
* SSH Terminal (Putty or Windows Terminal)

## Instructions

Install Firewall package. 
```shell
sudo apt install ufw
```

Enable UFW Firewall
```shell
ufw enable
```
Firewall Status
```shell
ufw status verbose
```
Check log in realtime
```shell
tail -f /var/log/ufw.log
```

### Configure Firewall Policies

Default policy creation
```shell
ufw allow ssh
ufw default deny incoming
```
Allow rule from IP and port
```shell
ufw allow from 15.15.15.0/24 to any port 22
```

Block from IP
```shell
ufw deny from 61.177.172.114/32 to any
```

Deleting rules
```shell
ufw delete allow 80
ufw delete allow 443
```