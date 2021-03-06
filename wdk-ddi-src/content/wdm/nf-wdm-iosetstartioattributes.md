---
UID: NF:wdm.IoSetStartIoAttributes
title: IoSetStartIoAttributes function
author: windows-driver-content
description: The IoSetStartIoAttributes routine sets attributes for the driver's StartIo routine.
old-location: kernel\iosetstartioattributes.htm
old-project: kernel
ms.assetid: 47ae3578-231c-49c8-a851-9f165db27fb1
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: IoSetStartIoAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available for Microsoft Windows XP and later versions of the Windows operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IoSetStartIoAttributes
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: StartIoCancel, StartIoRecursion, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any level
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# IoSetStartIoAttributes function



## -description
The <b>IoSetStartIoAttributes</b> routine sets attributes for the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff563858">StartIo</a> routine.



## -syntax

````
VOID IoSetStartIoAttributes(
  _In_ PDEVICE_OBJECT DeviceObject,
  _In_ BOOLEAN        DeferredStartIo,
  _In_ BOOLEAN        NonCancelable
);
````


## -parameters

### -param DeviceObject [in]

Pointer to the device object for the driver's device.


### -param DeferredStartIo [in]

If <b>TRUE</b>, the I/O manager will defer any call to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff563858">StartIo</a> routine while the driver is already inside the routine. In particular, if the <i>StartIo</i> routine calls <a href="..\ntifs\nf-ntifs-iostartnextpacket.md">IoStartNextPacket</a>, the <i>StartIo</i> routine will not be called again until the current invocation completes. The default is <b>FALSE</b>.


### -param NonCancelable [in]

If <b>TRUE</b>, the IRP cannot be canceled once it has been dequeued by a call to <b>IoStartNextPacket</b>. The default is <b>FALSE</b>. Drivers that set this member to <b>FALSE</b> must synchronize their IRP handling with the cancel spin lock.


## -returns
None


## -remarks


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563858">StartIo</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-iostartnextpacket.md">IoStartNextPacket</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IoSetStartIoAttributes routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

