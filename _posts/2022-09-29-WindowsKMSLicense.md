---
title: "Windows KMS Licensing"
date: 29-09-2022 14:00
categories: [Windows]
tags: [windows, licensing, server, kms]
---

# Summary
How to activate Windows Server licensing using KMS.

# Instructions

Set Server Edition
```console
DISM /online /Set-Edition:ServerStandard /ProductKey:N69G4-B89J2-4G8F4-WWYCC-J464C /AcceptEula
```

Install KMS Client Product key
```console
slmgr /ipk N69G4-B89J2-4G8F4-WWYCC-J464C
```
Set KMS Server
```console
slmgr.vbs -skms kms8.msguides.com
```
Activate Windows
```console
slmgr.vbs /ato
```