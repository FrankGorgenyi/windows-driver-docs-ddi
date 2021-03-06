---
UID: NF:ntifs.IoThreadToProcess
title: IoThreadToProcess function
author: windows-driver-content
description: The IoThreadToProcess routine returns a pointer to the process for the specified thread.
old-location: ifsk\iothreadtoprocess.htm
old-project: ifsk
ms.assetid: fcb51574-d966-4cd5-a946-c38dd2798b7f
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: IoThreadToProcess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IoThreadToProcess
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= DISPATCH_LEVEL
req.typenames: TOKEN_TYPE
---

# IoThreadToProcess function



## -description
The <b>IoThreadToProcess</b> routine returns a pointer to the process for the specified thread.



## -syntax

````
PEPROCESS IoThreadToProcess(
  _In_ PETHREAD Thread
);
````


## -parameters

### -param Thread [in]

Thread whose process is to be returned.


## -returns
<b>IoThreadToProcess</b> returns a pointer to the thread's process.

For more information about using system threads and managing synchronization within a nonarbitrary thread context, see <a href="https://msdn.microsoft.com/fbd8aadd-5a24-48c9-9865-80cc7dc97316">Driver Threads, Dispatcher Objects, and Resources</a>. 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\wdm\nf-wdm-iogetcurrentprocess.md">IoGetCurrentProcess</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559933">PsGetCurrentProcess</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-psgetcurrentthread.md">PsGetCurrentThread</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20IoThreadToProcess routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

