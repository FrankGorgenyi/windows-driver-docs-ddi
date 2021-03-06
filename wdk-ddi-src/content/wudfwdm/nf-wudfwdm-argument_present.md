---
UID: NF:wudfwdm.ARGUMENT_PRESENT
title: ARGUMENT_PRESENT macro
author: windows-driver-content
description: The ARGUMENT_PRESENT macro takes an argument pointer and returns FALSE if the pointer is NULL. Otherwise, it returns TRUE.
old-location: kernel\argument_present.htm
old-project: kernel
ms.assetid: 00b9c218-8ae7-4624-be6b-6b6b2f83764a
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: ARGUMENT_PRESENT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wudfwdm.h
req.include-header: Wdm.h, Ntddk.h, Ntdef.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: ARGUMENT_PRESENT
req.alt-loc: wudfwdm.h
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
req.typenames: *PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE
req.product: Windows 10 or later.
---

# ARGUMENT_PRESENT macro



## -description
The <b>ARGUMENT_PRESENT</b> macro takes an argument pointer and returns <b>FALSE</b> if the pointer is <b>NULL</b>. Otherwise, it returns <b>TRUE</b>.



## -syntax

````
BOOLEAN ARGUMENT_PRESENT(
  [in] CHAR *ArgumentPointer
);
````


## -parameters

### -param ArgumentPointer [in]

Specifies the value of the pointer argument to be tested.


## -remarks
This macro can be called in conditional code to determine whether an optional argument has been passed in a call. </p>