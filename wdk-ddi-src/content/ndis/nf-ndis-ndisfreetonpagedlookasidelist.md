---
UID: NF:ndis.NdisFreeToNPagedLookasideList
title: NdisFreeToNPagedLookasideList macro
author: windows-driver-content
description: The NdisFreeToNPagedLookasideList function returns an entry to the given lookaside list.
old-location: netvista\ndisfreetonpagedlookasidelist.htm
old-project: netvista
ms.assetid: 2405a405-177a-420a-9628-a340e0d0acb3
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: NdisFreeToNPagedLookasideList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Desktop
req.target-min-winverclnt: Supported for NDIS 6.0 and NDIS 5.1 drivers (see       NdisFreeToNPagedLookasideList (NDIS 5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see       NdisFreeToNPagedLookasideList (NDIS 5.1)) in Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: NdisFreeToNPagedLookasideList
req.alt-loc: ndis.h
req.ddi-compliance: Irql_Miscellaneous_Function
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: <= DISPATCH_LEVEL
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisFreeToNPagedLookasideList macro



## -description
The 
  <b>NdisFreeToNPagedLookasideList</b> function returns an entry to the given lookaside list.



## -syntax

````
VOID NdisFreeToNPagedLookasideList(
  [in] PNPAGED_LOOKASIDE_LIST Lookaside,
  [in] PVOID                  Entry
);
````


## -parameters

### -param Lookaside [in]

A pointer to the head of the lookaside list to which the entry will be returned.


### -param Entry [in]

A pointer to the entry to be freed.


## -remarks
If the lookaside list has not reached the system-determined maximum number of entries, 
    <i>Entry</i> is inserted at the front of the lookaside list. If the list has reached its maximum size, 
    <i>Entry</i> is released to nonpaged pool. That is, 
    <b>NdisFreeToNPagedLookasideList</b> either calls the driver's 
    <i>Free</i> function, specified in the 
    <i>Free</i> parameter if the driver provided one to the 
    <a href="..\ndis\nf-ndis-ndisinitializenpagedlookasidelist.md">
    NdisInitializeNPagedLookasideList</a> function, or it frees the given entry itself.


## -see-also
<dl>
<dt>
<a href="..\ndis\nf-ndis-ndisallocatefromnpagedlookasidelist.md">
   NdisAllocateFromNPagedLookasideList</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisdeletenpagedlookasidelist.md">
   NdisDeleteNPagedLookasideList</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisinitializenpagedlookasidelist.md">
   NdisInitializeNPagedLookasideList</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisFreeToNPagedLookasideList macro%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

