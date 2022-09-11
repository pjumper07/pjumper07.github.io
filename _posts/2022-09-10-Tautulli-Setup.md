---
title: "Tautulli Install & Configure"
date: 10-09-2022 14:00
categories: [Linux]
tags: [linux, install, config, tautulli]
---

# Summary 
How to install Tautulli on a Linux Debian/Ubuntu operating system via Git method. 

Original instructions taken from the Tautulli Github
https://github.com/Tautulli/Tautulli/wiki/Installation#linux

## Requirements
* Linux machine (Debian 11/Ubuntu)
* SSH Terminal (Putty or Windows Terminal)

## Instructions

Install Tautuilli step by step

Step 1 - prerequisites 
```shell
sudo apt-get install git python3 python3-setuptools python3-openssl
```
Step 2 - Change to /opt directory and clone Tautulli
```shell
cd /opt

sudo git clone https://github.com/Tautulli/Tautulli.git
```
Step 3 - Configure the Tautull user & update install folder ownership
```shell
sudo addgroup tautulli && sudo adduser --system --no-create-home tautulli --ingroup tautulli

sudo chown -R tautulli:tautulli /opt/Tautulli
```
Step 4 - Create, enable & start the Tautulli service.
```shell
sudo cp /opt/Tautulli/init-scripts/init.systemd /lib/systemd/system/tautulli.service

sudo systemctl daemon-reload && sudo systemctl enable tautulli.service

sudo systemctl start tautulli.service
```
Step 5 - Accessing your Tautulli via browser: 
http://localhost:8181

## Troubleshooting

Enabling SSL fails or keeps reverting after enabling, ensure the Python3 OpenSSL tools are installed these are required to enable SSL.

```shell
sudo apt-get install python3-openssl
```