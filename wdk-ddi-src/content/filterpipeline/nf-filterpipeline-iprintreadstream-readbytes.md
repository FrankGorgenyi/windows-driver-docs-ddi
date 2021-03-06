---
UID: NF:filterpipeline.IPrintReadStream.ReadBytes
title: IPrintReadStream::ReadBytes method
author: windows-driver-content
description: The ReadBytes method reads a number of bytes into a buffer.
old-location: print\iprintreadstream_readbytes.htm
old-project: print
ms.assetid: 41ba600d-8b89-4e07-950a-a2518c2572a6
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: IPrintReadStream, IPrintReadStream::ReadBytes, ReadBytes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: filterpipeline.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IPrintReadStream.ReadBytes
req.alt-loc: filterpipeline.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Filterpipeline.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
req.typenames: EXpsFontRestriction
---

# IPrintReadStream::ReadBytes method



## -description
The <code>ReadBytes</code> method reads a number of bytes into a buffer.



## -syntax

````
HRESULT ReadBytes(
  [out] void  *pvBuffer,
  [in]  ULONG cbRequested,
  [out] ULONG *pcbRead,
  [out] BOOL  *pbEndOfFile
);
````


## -parameters

### -param pvBuffer [out]

A pointer to the buffer that the bytes will be read into..


### -param cbRequested [in]

The number of bytes that are requested for the read.


### -param pcbRead [out]

A pointer to the number of bytes actually read.


### -param pbEndOfFile [out]

A pointer to a <b>BOOL</b> value that indicates whether the end of file (EOF) was read.


## -returns
<code>ReadBytes</code> returns an <b>HRESULT</b> value.


## -remarks
