---
UID: NS:hbaapi.HBA_FCPBinding2
title: HBA_FCPBinding2
author: windows-driver-content
description: The HBA_FCPBinding2 structure contains an array of bindings between operating system identifiers, SCSI logical unit ID descriptors (LUIDs) and fibre channel protocol (FCP) identifiers for a set of logical units.
old-location: storage\hba_fcpbinding2.htm
old-project: storage
ms.assetid: f715d45c-30e1-414f-907c-9ad1203ca604
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: HBA_FCPBinding2, HBA_FCPBINDING2, *PHBA_FCPBINDING2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hbaapi.h
req.include-header: Hbaapi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: HBA_FCPBINDING2
req.alt-loc: hbaapi.h
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
req.typenames: HBA_FCPBINDING2, *PHBA_FCPBINDING2
---

# HBA_FCPBinding2 structure



## -description
The HBA_FCPBinding2 structure contains an array of bindings between operating system identifiers, SCSI logical unit ID descriptors (LUIDs) and fibre channel protocol (FCP) identifiers for a set of logical units. 



## -syntax

````
typedef struct HBA_FCPBinding2 {
  HBA_UINT32           NumberOfEntries;
  HBA_FCPBINDINGENTRY2 entry[1];
} HBA_FCPBINDING2, *PHBA_FCPBINDING2;
````


## -struct-fields

### -field NumberOfEntries

Indicates, on input, the number of bindings that can fit in the array at <b>entry</b>. On output, this member holds the number of entries actually returned, which will be equal to the number specified on input or the full set of available bindings, whichever is smaller. The value in <b>NumberOfEntries</b> will contain the number of persistent bindings returned even when an error occurred because of insufficient buffer space. 


### -field entry

Variable length array of elements of type <a href="..\hbaapi\ns-hbaapi-hba_fcpbindingentry2.md">HBA_FCPBindingEntry2</a>, each of which holds a persistent binding between operating system identifiers, a SCSI logical unit ID descriptor (LUID) and a fibre channel protocol (FCP) identifier for a logical unit. 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\hbaapi\nf-hbaapi-hba_getpersistentbindingv2.md">HBA_GetPersistentBindingV2</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20HBA_FCPBinding2 structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

