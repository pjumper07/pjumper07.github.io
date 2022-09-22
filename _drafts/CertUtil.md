---
title: "CertUtil"
date: 10-09-2022 14:00
categories: [Windows]
tags: [windows, certificates, certutil]
---


# Summary 
How to use Windows CertUtil for managing certificates.


## Requirements
* Command Prompt (CMD or Windows Terminal)

## Instructions


List templates
```console
certutil -CATemplates -Config 
```

Request cert against template
```console
certreq -attrib "CertificateTemplate:WebServer"
```