---
UID: NS:ntddrilapitypes.RILPSMEDIACONFIGURATIONSET
title: RILPSMEDIACONFIGURATIONSET
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilpsmediaconfigurationset.htm
old-project: netvista
ms.assetid: b41f6539-293f-47ed-b720-5053574a1841
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RILPSMEDIACONFIGURATIONSET, RILPSMEDIACONFIGURATIONSET, *LPRILPSMEDIACONFIGURATIONSET
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddrilapitypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: RILPSMEDIACONFIGURATIONSET
req.alt-loc: ntddrilapitypes.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
req.typenames: RILPSMEDIACONFIGURATIONSET, *LPRILPSMEDIACONFIGURATIONSET
---

# RILPSMEDIACONFIGURATIONSET structure



## -description
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.



## -syntax

````
typedef struct _RILPSMEDIACONFIGURATIONSET {
  DWORD                       cbSize;
  DWORD                       dwExecutor;
  DWORD                       dwNumMediaConfiguration;
  RILPSMEDIACONFIGURATION [1] stMediaConfiguration;
} RILPSMEDIACONFIGURATIONSET, RILPSMEDIACONFIGURATIONSET;
````


## -struct-fields

### -field cbSize


### -field dwExecutor


### -field dwNumMediaConfiguration


### -field stMediaConfiguration


## -remarks
