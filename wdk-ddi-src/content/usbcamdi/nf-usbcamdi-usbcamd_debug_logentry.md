---
UID: NF:usbcamdi.USBCAMD_Debug_LogEntry
title: USBCAMD_Debug_LogEntry function
author: windows-driver-content
description: The USBCAMD_Debug_LogEntry function is called by the camera minidriver to log debugging information to a file.
old-location: stream\usbcamd_debug_logentry.htm
old-project: stream
ms.assetid: a718cf3e-8359-4560-a88e-dd7789b61be6
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: USBCAMD_Debug_LogEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: usbcamdi.h
req.include-header: Usbcamdi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: USBCAMD_Debug_LogEntry
req.alt-loc: usbcamd2.lib,usbcamd2.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usbcamd2.lib
req.dll: 
req.irql: 
req.typenames: USB_BUS_INTERFACE_USBDI_V3, *PUSB_BUS_INTERFACE_USBDI_V3
req.product: Windows 10 or later.
---

# USBCAMD_Debug_LogEntry function



## -description
The <b>USBCAMD_Debug_LogEntry</b> function is called by the camera minidriver to log debugging information to a file.



## -syntax

````
VOID USBCAMD_Debug_LogEntry(
  _In_ CHAR  *Name,
  _In_ ULONG Info1,
  _In_ ULONG Info2,
  _In_ ULONG Info3
);
````


## -parameters

### -param Name [in]

Pointer to a <b>NULL</b>-terminated string containing the name of the file to write the log entry to.


### -param Info1 [in]

Specifies the first information value to be written to the log file.


### -param Info2 [in]

Specifies the second information value to be written to the log file.


### -param Info3 [in]

Specifies the third information value to be written to the log file.


## -returns
<b>USBCAMD_Debug_LogEntry </b>does not return a value.


## -remarks
The original USBCAMD does not call <b>USBCAMD_Debug_LogEntry</b>.</p>