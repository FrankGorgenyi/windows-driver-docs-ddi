---
UID: NS:bthddi._BRB_ACL_GET_MODE
title: _BRB_ACL_GET_MODE
author: windows-driver-content
description: The _BRB_ACL_GET_MODE structure describes the ACL mode for the specified remote device.
old-location: bltooth\_brb_acl_get_mode.htm
old-project: bltooth
ms.assetid: 2fe473c8-dcf9-4457-b1b1-c55b3eaa68e6
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: _BRB_ACL_GET_MODE,
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bthddi.h
req.include-header: Bthddi.h
req.target-type: Windows
req.target-min-winverclnt: Versions: Supported in Windows Vista, and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: _BRB_ACL_GET_MODE
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
req.typenames: 
---

# _BRB_ACL_GET_MODE structure



## -description
The _BRB_ACL_GET_MODE structure describes the ACL mode for the specified remote device.



## -syntax

````
struct _BRB_ACL_GET_MODE {
  BRB_HEADER Hdr;
  BTH_ADDR   BtAddress;
  ACL_MODE   AclMode;
};
````


## -struct-fields

### -field Hdr

A 
     <a href="..\bthddi\ns-bthddi-_brb_header.md">BRB_HEADER</a> structure that contains information
     about the current BRB.


### -field BtAddress

The address of the remote device.


### -field AclMode

A value from the 
     <a href="..\bthddi\ne-bthddi-_acl_mode.md">ACL_MODE</a> enumeration that specifies the ACL mode of
     the remote device.


## -remarks
To get the current ACL connection state for a remote device, profile drivers should 
    <a href="https://msdn.microsoft.com/53a692e7-9c71-4dca-9331-32ac97b94179">build and send</a> a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff536609">BRB_ACL_GET_MODE</a> request.


## -see-also
<dl>
<dt>
<a href="..\bthddi\ns-bthddi-_brb_header.md">BRB_HEADER</a>
</dt>
<dt>
<a href="..\bthddi\ne-bthddi-_acl_mode.md">ACL_MODE</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536609">BRB_ACL_GET_MODE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [bltooth\bltooth]:%20_BRB_ACL_GET_MODE structure%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

