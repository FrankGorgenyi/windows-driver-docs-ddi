---
UID: NF:printerextension.IPrintSchemaTicket.ValidateAsync
title: IPrintSchemaTicket::ValidateAsync method
author: windows-driver-content
description: Gets an asynchronous PrintTicket validation operation context.
old-location: print\iprintschematicket_validateasync.htm
old-project: print
ms.assetid: B46AE68A-36E1-4367-95F5-0FFBAA42171C
ms.author: windowsdriverdev
ms.date: 1/8/2018
ms.keywords: IPrintSchemaTicket, IPrintSchemaTicket::ValidateAsync, ValidateAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IPrintSchemaTicket.ValidateAsync
req.alt-loc: printerextension.h
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

# IPrintSchemaTicket::ValidateAsync method



## -description
Gets an asynchronous PrintTicket validation operation context.



## -syntax

````
HRESULT ValidateAsync(
  [out] IPrintSchemaAsyncOperation **ppAsyncOperation
);
````


## -parameters

### -param ppAsyncOperation [out]

The asynchronous validation operation context.


## -returns
This method returns an <b>HRESULT</b> value.


## -remarks
 To perform the validation operation, call the <a href="https://msdn.microsoft.com/8AEA34AA-1A5E-43F6-8EE1-B1A078B6AEA3">IPrintSchemaAsyncOperation::Start</a> method to validate the settings of the current PrintTicket object and to pass the resulting PrintTicket to the <a href="https://msdn.microsoft.com/B1599F21-D6DD-497D-9CD8-6C637ABAA33A">IPrintSchemaAsyncOperationEvent::Completed</a> event. When the validation operation is completed, or if an error occurs during the validation operation, the <b>IPrintSchemaAsyncOperationEvent::Completed</b> event is fired. This method will not change the settings of the current PrintTicket object.


## -see-also
<dl>
<dt>
<a href="..\printerextension\nn-printerextension-iprintschematicket.md">IPrintSchemaTicket</a>
</dt>
<dt>
<a href="..\printerextension\nn-printerextension-iprintschemaasyncoperation.md">IPrintSchemaAsyncOperation</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/8AEA34AA-1A5E-43F6-8EE1-B1A078B6AEA3">IPrintSchemaAsyncOperation::Start</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/B1599F21-D6DD-497D-9CD8-6C637ABAA33A">IPrintSchemaAsyncOperationEvent::Completed</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrintSchemaTicket::ValidateAsync method%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

