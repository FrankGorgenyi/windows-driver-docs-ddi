---
UID: NF:storport.StorPortWriteRegisterBufferUlong64
title: StorPortWriteRegisterBufferUlong64 macro
author: windows-driver-content
description: This StorPortWriteRegisterBufferUlong64 routine writes a number of ULONG64 values from a the specified 64-bit register address.
old-location: storage\storportwriteregisterbufferulong64.htm
old-project: storage
ms.assetid: 3C36DB8F-46C2-4E81-B2F3-6DE78D91566E
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: StorPortWriteRegisterBufferUlong64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: StorPortWriteRegisterBufferUlong64
req.alt-loc: storport.h
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
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---

# StorPortWriteRegisterBufferUlong64 macro



## -description
This <b>StorPortWriteRegisterBufferUlong64</b> routine writes a number of <b>ULONG64</b> values from a the specified 64-bit register address.
 



## -syntax

````
 VOID StorPortWriteRegisterBufferUlong64(
  _In_ PULONG64  Register,
  _In_ PULONG64  Buffer,
  _In_ ULONG     Count
);
````


## -parameters

### -param Register [in]

Pointer to the register where the data is written to. The register must be a mapped range in memory space


### -param Buffer [in]

Pointer to the buffer to write the <b>ULONG64</b> values from.


### -param Count [in]

Specifies the number of data values to write. Each data item has a size of <b>sizeof</b>(ULONG64). 


## -remarks
The <b>StorPortWriteRegisterBufferUlong64</b> routine is only available on the 64-bit version of Windows.


## -see-also
<dl>
<dt>
<a href="..\storport\nf-storport-storportreadregisterbufferulong64.md">StorPortReadRegisterBufferUlong64</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortWriteRegisterBufferUlong64 routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

