---
title: API
layout: rancher-api-default
version: v1.2
lang: en
---

## credential





### Resource Fields

Field | Type | Required | Default | Description
---|---|---|---|---
description | string | false |  | 
id | int | false |  | The unique identifier for the credential
name | string | false |  | 
publicValue | string | false |  | The public value of the credential
secretValue | [password]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/password/) | false |  | The secret value of the credential

