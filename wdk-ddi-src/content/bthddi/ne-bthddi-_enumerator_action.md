---
UID: NE:bthddi._ENUMERATOR_ACTION
title: _ENUMERATOR_ACTION
author: windows-driver-content
description: Reserved for internal use.
old-location: bltooth\enumerator_action.htm
old-project: bltooth
ms.assetid: d5acaec6-7b3b-4dd9-8901-f96b4e49149f
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: _ENUMERATOR_ACTION, ENUMERATOR_ACTION, *PENUMERATOR_ACTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: bthddi.h
req.include-header: Bthddi.h
req.target-type: Windows
req.target-min-winverclnt: Versions: Supported in Windows Vista, and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: ENUMERATOR_ACTION
req.alt-loc: bthddi.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: Developers should code this function to operate at either IRQL = DISPATCH_LEVEL (if the callback   function does not access paged memory), or IRQL = PASSIVE_LEVEL (if the callback function must access   paged memory)
req.typenames: ENUMERATOR_ACTION, *PENUMERATOR_ACTION
---

# _ENUMERATOR_ACTION enumeration



## -description
Reserved for internal use.



## -syntax

````
typedef enum _ENUMERATOR_ACTION { 
  ENUMERATOR_ACTION_CREATE,
  ENUMERATOR_ACTION_REMOVE,
  ENUMERATOR_ACTION_DESTROY,
  ENUMERATOR_ACTION_MAX
}  *ENUMERATOR_ACTION, *PENUMERATOR_ACTION;
````


## -enum-fields

### -field ENUMERATOR_ACTION_CREATE

Reserved.


### -field ENUMERATOR_ACTION_REMOVE

Reserved.


### -field ENUMERATOR_ACTION_DESTROY

Reserved.


### -field ENUMERATOR_ACTION_MAX

Reserved.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\bthddi\ns-bthddi-_brb.md">BRB</a>
</dt>
<dt>
<a href="..\bthddi\ns-bthddi-_brb_header.md">BRB_HEADER</a>
</dt>
<dt>
<a href="..\bthddi\nc-bthddi-pfnbth_allocate_brb.md">BthAllocateBrb</a>
</dt>
<dt>
<a href="..\bthddi\nc-bthddi-pfnbth_initialize_brb.md">BthInitializeBrb</a>
</dt>
<dt>
<a href="..\bthioctl\ni-bthioctl-ioctl_internal_bth_submit_brb.md">IOCTL_INTERNAL_BTH_SUBMIT_BRB</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [bltooth\bltooth]:%20ENUMERATOR_ACTION Enumeration enumeration%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

