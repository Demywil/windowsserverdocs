---
title: ksetup:delenctypeattr
description: Reference topic for **** - 

ms.prod: windows-server


ms.technology: manage-windows-commands

ms.topic: article
ms.assetid: 4fc25ef3-e271-4229-a712-72c507df55aa
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
---

# ksetup:delenctypeattr



Removes the encryption type attribute for the domain.

## Syntax

```
ksetup /delenctypeattr <DomainName> 
```

#### Parameters

|Parameter|Description|
|---------|-----------|
|\<DomainName>|Name of the domain to which you want to establish a connection. Use the fully qualified domain name or a simple form of the name, such as corp.contoso.com or contoso.|

## Remarks

To view the encryption type for the Kerberos ticket-granting ticket (TGT) and the session key, run the **klist** command and view the output.

A status message is displayed upon successful or failed completion.

To set the domain that you want to connect to and use, run the **ksetup /domain \<DomainName>** command.

## Examples

Determine the current encryption types that are set on this computer:
```
klist
```
Set the domain to mit.contoso.com:
```
ksetup /domain mit.contoso.com
```
Verify what the encryption type attribute is for the domain:
```
ksetup /getenctypeattr mit.contoso.com
```
Remove the set encryption type attribute for the domain mit.contoso.com:
```
ksetup /delenctypeattr mit.contoso.com
```

## Additional References

-   [Klist](klist.md)
-   [Ksetup:domain](ksetup-domain.md)
-   [Ksetup:addenctypeattr](ksetup-addenctypeattr.md)
-   [Ksetup:setenctypeattr](ksetup-setenctypeattr.md)
-   [Ksetup:delenctypeattr](ksetup-delenctypeattr.md)
-   - [Command-Line Syntax Key](command-line-syntax-key.md)