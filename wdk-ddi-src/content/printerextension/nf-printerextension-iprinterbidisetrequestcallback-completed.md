---
UID: NF:printerextension.IPrinterBidiSetRequestCallback.Completed
title: IPrinterBidiSetRequestCallback::Completed method
author: windows-driver-content
description: Invoked when the Bidi “Set”” operation is completed.
old-location: print\iprinterbidisetrequestcallback_completed.htm
old-project: print
ms.assetid: F086903F-2FCA-4B9F-948B-0F40F114E11D
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: IPrinterBidiSetRequestCallback, IPrinterBidiSetRequestCallback::Completed, Completed
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IPrinterBidiSetRequestCallback.Completed
req.alt-loc: Printerextension.h
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
req.typenames: PrintSchemaSelectionType
req.product: Windows 10 or later.
---

# IPrinterBidiSetRequestCallback::Completed method



## -description
Invoked when the Bidi “Set”” operation is completed.



## -syntax

````
HRESULT Completed(
  [in] BSTR    bstrResponse,
  [in] HRESULT hrStatus
);
````


## -parameters

### -param bstrResponse [in]

The received response.


### -param hrStatus [in]

An HRESULT value.


## -returns
This method returns the appropriate <b>HRESULT</b> value.


## -remarks


## -see-also
<dl>
<dt>
<a href="..\printerextension\nn-printerextension-iprinterbidisetrequestcallback.md">IPrinterBidiSetRequestCallback</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrinterBidiSetRequestCallback::Completed method%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

