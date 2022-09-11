---
title: "Windows 11 TPM Bypass"
date: 10-09-2022 14:00
categories: [Windows]
tags: [windows, install, config]
---

# Summary
How to bypass TPM Requirements for Windows 11. 

## Requirements
* Windows 11 (console access)


# Instructions

* Press Shift + F10
* A DOS box appears. Typ regedit and hit enter
* Navigate to HKEY_LOCAL_MACHINE\SYSTEM\Setup and create a new Key named LabConfig
* Create in the LabConfig Key a ByPassTPMCheck DWORD (32-bit) with the value of 1
* Close the Regedit window (click on the Red X in the right corner)
* Type exit to leave the command prompt
* Click on the Red X in the right corner and the setup will start again