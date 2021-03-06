---
UID: NF:wdm.KeGetProcessorNumberFromIndex
title: KeGetProcessorNumberFromIndex function
author: windows-driver-content
description: The KeGetProcessorNumberFromIndex routine converts a systemwide processor index to a group number and a group-relative processor number.
old-location: kernel\kegetprocessornumberfromindex.htm
old-project: kernel
ms.assetid: a6c9a7fa-8fef-4d6d-aab5-e712c49c0144
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: KeGetProcessorNumberFromIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h, Ntddk.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KeGetProcessorNumberFromIndex
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
req.irql: Any level
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# KeGetProcessorNumberFromIndex function



## -description
The <b>KeGetProcessorNumberFromIndex</b> routine converts a systemwide processor index to a group number and a group-relative processor number.



## -syntax

````
NTSTATUS KeGetProcessorNumberFromIndex(
  _In_  ULONG             ProcIndex,
  _Out_ PPROCESSOR_NUMBER ProcNumber
);
````


## -parameters

### -param ProcIndex [in]

A systemwide processor index. If a multiprocessor system contains a total of <i>n</i> logical processors, valid processor indexes range from 0 to <i>n</i>-1. 


### -param ProcNumber [out]

A pointer to a caller-allocated <a href="..\miniport\ns-miniport-_processor_number.md">PROCESSOR_NUMBER</a> structure into which the routine writes the group number and group-relative processor number of the processor that is identified by <i>ProcIndex</i>. 


## -returns
<b>KeGetProcessorNumberFromIndex</b> returns STATUS_SUCCESS if the call is successful. Possible error return values include the following:
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>The <i>ProcIndex</i> parameter value is not a valid processor index.

 


## -remarks
This routine accepts as input a processor index that identifies the processor across the entire multiprocessor system. The output value is a <b>PROCESSOR_NUMBER</b> structure that identifies a processor by its group number and its processor number within the group.

For example, if a multiprocessor system contains two groups, and each group contains 64 logical processors, the processor numbers in each group range from 0 to 63, but the systemwide processor indexes range from 0 to 127.

To obtain the total number of active logical processors in the system, call the <a href="..\ntddk\nf-ntddk-kequeryactiveprocessorcountex.md">KeQueryActiveProcessorCountEx</a> routine.

The <a href="..\ntifs\nf-ntifs-kegetprocessorindexfromnumber.md">KeGetProcessorIndexFromNumber</a> routine converts a group number and a group-relative processor number to a systemwide processor index.

The following code example uses the <b>KeQueryActiveProcessorCountEx</b> and <b>KeGetProcessorNumberFromIndex</b> routines to enumerate all active logical processors in the system:

The constant value ALL_PROCESSOR_GROUPS is defined in Winnt.h and Ntdef.h. 


## -see-also
<dl>
<dt>
<a href="..\ntifs\nf-ntifs-kegetprocessorindexfromnumber.md">KeGetProcessorIndexFromNumber</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-kequeryactiveprocessorcountex.md">KeQueryActiveProcessorCountEx</a>
</dt>
<dt>
<a href="..\miniport\ns-miniport-_processor_number.md">PROCESSOR_NUMBER</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20KeGetProcessorNumberFromIndex routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

