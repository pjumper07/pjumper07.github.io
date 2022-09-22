---
title: "Remote PowerShell"
date: 10-09-2022 14:00
categories: [Windows]
tags: [windows, powershell]
---


# Summary 
How to use PowerShell for connecting to Remote Computers.


## Requirements
* Command Prompt (CMD or Windows Terminal)

## Instructions


List PowerShell Sessions
```powershell
Get-PSSession
```

Create PowerShell Session to remote computer. 
```powershell
New-PSSession -ComputerName namehere
```

Enter PowerShell sessions to remote computer. 
```powershell
Enter-PSSession -ComputerName namehere
```

Delete PowerShell session to remote computer.
```powershell
Remove-PSSession -ComputerName namehere
```