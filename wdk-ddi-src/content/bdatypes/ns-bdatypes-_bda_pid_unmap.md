---
UID: NS:bdatypes._BDA_PID_UNMAP
title: _BDA_PID_UNMAP
author: windows-driver-content
description: The BDA_PID_UNMAP structure describes packet types to stop filtering from the input stream of a packet identifier (PID) filter. These packet types are identified with PIDs.
old-location: stream\bda_pid_unmap.htm
old-project: stream
ms.assetid: 7c669708-9b5d-424f-ab6f-6e3498331c74
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: _BDA_PID_UNMAP, BDA_PID_UNMAP, *PBDA_PID_UNMAP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: Bdatypes.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: BDA_PID_UNMAP
req.alt-loc: bdatypes.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.typenames: BDA_PID_UNMAP, *PBDA_PID_UNMAP
---

# _BDA_PID_UNMAP structure



## -description
The BDA_PID_UNMAP structure describes packet types to stop filtering from the input stream of a packet identifier (PID) filter. These packet types are identified with PIDs. 



## -syntax

````
typedef struct _BDA_PID_UNMAP {
  ULONG ulcPIDs;
  ULONG aulPIDs[MIN_DIMENSION];
} BDA_PID_UNMAP, *PBDA_PID_UNMAP;
````


## -struct-fields

### -field ulcPIDs

Number of PIDs in the <b>aulPIDs</b> array. 


### -field aulPIDs

Array of PIDs that identify packets to unmap from the output of a PID filter. 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\bdatypes\ns-bdatypes-_bda_pid_map.md">BDA_PID_MAP</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566551">KSPROPSETID_BdaPIDFilter</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff567719">MEDIA_SAMPLE_CONTENT</a>
</dt>
<dt>
<a href="..\bdatypes\ns-bdatypes-pid_map.md">PID_MAP</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20BDA_PID_UNMAP structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

