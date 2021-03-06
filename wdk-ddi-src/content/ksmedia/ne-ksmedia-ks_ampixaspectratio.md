---
UID: NE:ksmedia.KS_AMPixAspectRatio
title: KS_AMPixAspectRatio
author: windows-driver-content
description: The KS_AMPixAspectRatio enumeration defines the pixel aspect ratio that corresponds to a 720 480 NTSC video signal or a 720 × 576 PAL video signal.
old-location: stream\ks_ampixaspectratio.htm
old-project: stream
ms.assetid: 29c84529-11f6-429b-81c6-96d6a1773b3b
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: KS_AMPixAspectRatio, KS_AMPixAspectRatio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KS_AMPixAspectRatio
req.alt-loc: ksmedia.h
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
req.typenames: KS_AMPixAspectRatio
---

# KS_AMPixAspectRatio enumeration



## -description
The KS_AMPixAspectRatio enumeration defines the pixel aspect ratio that corresponds to a 720  480 NTSC video signal or a 720 × 576 PAL video signal.



## -syntax

````
typedef enum  { 
  KS_PixAspectRatio_NTSC4x3   = 0,
  KS_PixAspectRatio_NTSC16x9  = 1,
  KS_PixAspectRatio_PAL4x3    = 2,
  KS_PixAspectRatio_PAL16x9   = 3
} KS_AMPixAspectRatio;
````


## -enum-fields

### -field KS_PixAspectRatio_NTSC4x3

Specifies a 4 × 3 NTSC pixel aspect ratio.


### -field KS_PixAspectRatio_NTSC16x9

Specifies a 16 × 9 NTSC pixel aspect ratio.


### -field KS_PixAspectRatio_PAL4x3

Specifies a 4 × 3 PAL pixel aspect ratio.


### -field KS_PixAspectRatio_PAL16x9

Specifies a 16 × 9 PAL pixel aspect ratio.


## -remarks
