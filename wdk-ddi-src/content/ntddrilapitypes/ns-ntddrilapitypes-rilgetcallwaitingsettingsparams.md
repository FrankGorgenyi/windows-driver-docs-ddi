---
UID: NS:ntddrilapitypes.RILGETCALLWAITINGSETTINGSPARAMS
title: RILGETCALLWAITINGSETTINGSPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilgetcallwaitingsettingsparams.htm
old-project: netvista
ms.assetid: b257ef88-a474-4443-8fbf-91759066a536
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: RILGETCALLWAITINGSETTINGSPARAMS, *LPRILGETCALLWAITINGSETTINGSPARAMS, RILGETCALLWAITINGSETTINGSPARAMS
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
req.alt-api: RILGETCALLWAITINGSETTINGSPARAMS
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
req.typenames: *LPRILGETCALLWAITINGSETTINGSPARAMS, RILGETCALLWAITINGSETTINGSPARAMS
---

# RILGETCALLWAITINGSETTINGSPARAMS structure



## -description
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.



## -syntax

````
typedef struct _RILGETCALLWAITINGSETTINGSPARAMS {
  DWORD  dwExecutor;
  BOOL   fAllClasses;
  DWORD  dwInfoClasses;
} RILGETCALLWAITINGSETTINGSPARAMS, RILGETCALLWAITINGSETTINGSPARAMS;
````


## -struct-fields

### -field dwExecutor


### -field fAllClasses


### -field dwInfoClasses


## -remarks
