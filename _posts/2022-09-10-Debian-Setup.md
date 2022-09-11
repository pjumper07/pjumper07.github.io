---
title: "Debian Setup & Configure"
date: 10-09-2022 14:00
categories: [Linux]
tags: [linux, install, config, debian]
---

# Summary 
How to configure a Debian operating system to be ready for use, post-OS install. 

## Requirements
* Debian Linux (lightweight install)
* SSH Terminal (Putty or Windows Terminal)

## Instructions

### Initial config
Step 1 - Ensure all sources and packages are fully updated. 
```shell
apt-get update
apt-get upgrade
```
Step 2 - Install sudo package. 
```shell
apt-get install sudo
```
Step 3 (optional) - Enable SSH for root account
```console
sudo nano /etc/ssh/sshd_config

uncomment and edit theline "PermitRootLogin yes"
```

### Configure Static IP Address
```shell
sudo nano /etc/network/interfaces

edit the line: 
iface ens192 inet static
address 192.168.0.1
netmask 255.255.255.0
gateway 192.168.0.254
dns-nameservers 192.168.0.254
```

### Add Root CA Certs
Copy all CA certs to: /usr/local/share/ca-certificates/
```shell
update-ca-certificate
```

### Configure NTP Settings
Install NTP Client
```shell
sudo apt install ntp
```

Edit NTP Config
```shell
sudo nano /etc/ntp.conf

add line to config file:
server 192.168.0.254 prefer iburst
```

Check NTP status
```shell
ntpq -p
```
