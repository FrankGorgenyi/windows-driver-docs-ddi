---
UID: NS:ntddcdrm._CDROM_TOC_FULL_TOC_DATA
title: _CDROM_TOC_FULL_TOC_DATA
author: windows-driver-content
description: Device control IRPs with a control code of IOCTL_CDROM_READ_TOC_EX and a format of CDROM_READ_TOC_EX_FORMAT_FULL_TOC return their output data in this structure optionally followed by a series of descriptors of type CDROM_TOC_FULL_TOC_DATA_BLOCK.
old-location: storage\cdrom_toc_full_toc_data.htm
old-project: storage
ms.assetid: c82e08e5-1450-40a3-a25a-49eefc7bc887
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: _CDROM_TOC_FULL_TOC_DATA, *PCDROM_TOC_FULL_TOC_DATA, CDROM_TOC_FULL_TOC_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddcdrm.h
req.include-header: Ntddcdrm.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: CDROM_TOC_FULL_TOC_DATA
req.alt-loc: ntddcdrm.h
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
req.typenames: *PCDROM_TOC_FULL_TOC_DATA, CDROM_TOC_FULL_TOC_DATA
---

# _CDROM_TOC_FULL_TOC_DATA structure



## -description
Device control IRPs with a control code of <a href="..\ntddcdrm\ni-ntddcdrm-ioctl_cdrom_read_toc_ex.md">IOCTL_CDROM_READ_TOC_EX</a> and a format of CDROM_READ_TOC_EX_FORMAT_FULL_TOC return their output data in this structure optionally followed by a series of descriptors of type <a href="..\ntddcdrm\ns-ntddcdrm-_cdrom_toc_full_toc_data_block.md">CDROM_TOC_FULL_TOC_DATA_BLOCK</a>. 



## -syntax

````
typedef struct _CDROM_TOC_FULL_TOC_DATA {
  UCHAR                         Length[2];
  UCHAR                         FirstCompleteSession;
  UCHAR                         LastCompleteSession;
  CDROM_TOC_FULL_TOC_DATA_BLOCK Descriptors[];
} CDROM_TOC_FULL_TOC_DATA, *PCDROM_TOC_FULL_TOC_DATA;
````


## -struct-fields

### -field Length

Indicates the length, in bytes, of the table of contents data. This length value does not include the length of the <b>Length </b>member itself. 


### -field FirstCompleteSession

Contains the number of the first complete session. 


### -field LastCompleteSession

Contains the number of last complete session. 


### -field Descriptors

Contains zero or more track descriptors. See <a href="..\ntddcdrm\ns-ntddcdrm-_cdrom_toc_full_toc_data_block.md">CDROM_TOC_FULL_TOC_DATA_BLOCK</a> for a description of the track descriptor. 


## -remarks


## -see-also
<dl>
<dt>
<a href="..\ntddcdrm\ni-ntddcdrm-ioctl_cdrom_read_toc_ex.md">IOCTL_CDROM_READ_TOC_EX</a>
</dt>
<dt>
<a href="..\ntddcdrm\ns-ntddcdrm-_cdrom_read_toc_ex.md">CDROM_READ_TOC_EX</a>
</dt>
<dt>
<a href="..\ntddcdrm\ns-ntddcdrm-_cdrom_toc_full_toc_data_block.md">CDROM_TOC_FULL_TOC_DATA_BLOCK</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20CDROM_TOC_FULL_TOC_DATA structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

