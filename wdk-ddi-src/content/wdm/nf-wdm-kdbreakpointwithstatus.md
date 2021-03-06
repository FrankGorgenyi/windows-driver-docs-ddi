---
UID: NF:wdm.KdBreakPointWithStatus
title: KdBreakPointWithStatus macro
author: windows-driver-content
description: The KdBreakPointWithStatus macro breaks into the kernel debugger and sends the value of Status to the debugger.
old-location: devtest\kdbreakpointwithstatus.htm
old-project: devtest
ms.assetid: 0b7f2f55-f7b8-415b-b683-3b6b96f84eb3
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: KdBreakPointWithStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KdBreakPointWithStatus
req.alt-loc: ntddk.h
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
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# KdBreakPointWithStatus macro



## -description
The <b>KdBreakPointWithStatus</b> macro breaks into the kernel debugger and sends the value of <i>Status</i> to the debugger.



## -syntax

````
NTSYSAPI VOID
NTAPI KdBreakPointWithStatus(
  _In_ ULONG Status
);
````


## -parameters

### -param Status [in]

Specifies a ULONG value to be sent to the debugger (for example, a status code or an address).


## -remarks
<b>KdBreakPointWithStatus</b> is identical to the <a href="..\wdm\nf-wdm-dbgbreakpointwithstatus.md">DbgBreakPointWithStatus</a> routine in code that is compiled for a debug configuration. This routine has no effect if compiled in a release configuration.

On x86 computers, the <i>Status</i> parameter is stored in the <b>eax</b> register. On computers that have register calling conventions, <i>Status</i> is stored in the first argument register.

This routine raises an exception that is handled by the kernel debugger if one is installed; otherwise it is handled by the debug system. If a debugger is not connected to the system, the exception can be handled in the standard way.

In kernel mode, a break exception that is not handled will cause a bug check. You can, however, connect a kernel-mode debugger to a target computer that has stopped responding and has kernel debugging enabled. For more information, see <a href="https://msdn.microsoft.com/938ef180-84de-442f-9b6c-1138c2fc8d5a">Windows Debugging</a>.


## -see-also
<dl>
<dt>
<a href="..\wdm\nf-wdm-dbgbreakpoint.md">DbgBreakPoint</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-dbgbreakpointwithstatus.md">DbgBreakPointWithStatus</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff548063">KdBreakPoint</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/938ef180-84de-442f-9b6c-1138c2fc8d5a">Windows Debugging</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [devtest\devtest]:%20KdBreakPointWithStatus function%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

