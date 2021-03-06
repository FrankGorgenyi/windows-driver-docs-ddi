---
UID: NE:ntddcdvd.DVD_STRUCTURE_FORMAT
title: DVD_STRUCTURE_FORMAT
author: windows-driver-content
description: The DVD_STRUCTURE_FORMAT enumeration type is used in conjunction with the IOCTL_DVD_READ_STRUCTURE request and the DVD_READ_STRUCTURE structure to retrieve a DVD descriptor.
old-location: storage\dvd_structure_format.htm
old-project: storage
ms.assetid: 0f3ca59b-f7e9-4bd7-a652-f7f0a6075d80
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: DVD_STRUCTURE_FORMAT, *PDVD_STRUCTURE_FORMAT, DVD_STRUCTURE_FORMAT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddcdvd.h
req.include-header: Ntddcdvd.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: DVD_STRUCTURE_FORMAT
req.alt-loc: ntddcdvd.h
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
req.typenames: *PDVD_STRUCTURE_FORMAT, DVD_STRUCTURE_FORMAT
---

# DVD_STRUCTURE_FORMAT enumeration



## -description
The DVD_STRUCTURE_FORMAT enumeration type is used in conjunction with the <a href="..\ntddcdvd\ni-ntddcdvd-ioctl_dvd_read_structure.md">IOCTL_DVD_READ_STRUCTURE</a> request and the <a href="..\ntddcdvd\ns-ntddcdvd-dvd_read_structure.md">DVD_READ_STRUCTURE</a> structure to retrieve a DVD descriptor.



## -syntax

````
typedef enum DVD_STRUCTURE_FORMAT { 
  DvdPhysicalDescriptor      = 0,
  DvdCopyrightDescriptor     = 1,
  DvdDiskKeyDescriptor       = 2,
  DvdBCADescriptor           = 3,
  DvdManufacturerDescriptor  = 4,
  DvdMaxDescriptor           = 5
} DVD_STRUCTURE_FORMAT, *PDVD_STRUCTURE_FORMAT;
````


## -enum-fields

### -field DvdPhysicalDescriptor

Indicates that caller is requesting a DVD physical descriptor. 


### -field DvdCopyrightDescriptor

Indicates that caller is requesting a DVD copyright descriptor containing copyright information from the DVD lead-in area. 


### -field DvdDiskKeyDescriptor

Indicates that caller is requesting a DVD key descriptor containing the disc key obfuscated using the bus key. 


### -field DvdBCADescriptor

Indicates that caller is requesting a DVD burst cutting area (BCA) descriptor. 


### -field DvdManufacturerDescriptor

Indicates that caller is requesting a DVD manufacturer descriptor containing disc manufacturing information from the DVD lead-in area. 


### -field DvdMaxDescriptor

Indicates that caller is requesting a DVD max descriptor. 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\ntddcdvd\ns-ntddcdvd-dvd_read_structure.md">DVD_READ_STRUCTURE</a>
</dt>
<dt>
<a href="..\ntddcdvd\ni-ntddcdvd-ioctl_dvd_read_structure.md">IOCTL_DVD_READ_STRUCTURE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20DVD_STRUCTURE_FORMAT enumeration%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

