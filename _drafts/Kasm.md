---
title: "Kasm SSL"
date: 10-09-2022 14:00
categories: [Linux]
tags: [linux, kasm]
---


# Summary
How to configure Kasm with SSL

# Instructions

Stop Kasm Services
```shell
sudo /opt/kasm/bin/stop
```

Replace certificate
```shell
sudo cp cfwild.crt /opt/kasm/current/certs/kasm_nginx.crt
sudo cp cfwild.key /opt/kasm/current/certs/kasm_nginx.key
```
Start Kasm Services
```shell
sudo /opt/kasm/bin/start
```