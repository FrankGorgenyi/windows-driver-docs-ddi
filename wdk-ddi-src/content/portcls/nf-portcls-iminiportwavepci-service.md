---
UID: NF:portcls.IMiniportWavePci.Service
title: IMiniportWavePci::Service method
author: windows-driver-content
description: The Service method notifies the miniport driver of a request for service.
old-location: audio\iminiportwavepci_service.htm
old-project: audio
ms.assetid: 1c30293f-1516-47a7-bb2c-29f9dc682777
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IMiniportWavePci, IMiniportWavePci::Service, Service
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portcls.h
req.include-header: Portcls.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IMiniportWavePci.Service
req.alt-loc: portcls.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: DISPATCH_LEVEL
req.typenames: PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IMiniportWavePci::Service method



## -description
The <code>Service</code> method notifies the miniport driver of a request for service.



## -syntax

````
void Service(
    None
);
````


## -parameters

### -param None 


## -returns
None


## -remarks
When the port driver calls the miniport driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff536734">IMiniportWavePci::Init</a> method, that method outputs a reference to the miniport driver's <a href="..\portcls\nn-portcls-iservicegroup.md">IServiceGroup</a> object. The port driver adds its own <a href="..\portcls\nn-portcls-iservicesink.md">IServiceSink</a> object to this service group and awaits notification of a service request. The source of the notification is typically the miniport driver's interrupt service routine (ISR).

When the miniport driver's ISR calls the port driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff536918">IPortWavePci::Notify</a> routine, the port driver queues a deferred procedure call (DPC). When the DPC executes, it calls the <b>RequestService</b> method on each of the <b>IServiceSink</b> objects in the service group. When the DPC calls this method on the port driver's <b>IServiceSink</b> object, the port driver in turn calls the miniport driver's <code>Service</code> method.


## -see-also
<dl>
<dt>
<a href="..\portcls\nn-portcls-iminiportwavepci.md">IMiniportWavePci</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536734">IMiniportWavePci::Init</a>
</dt>
<dt>
<a href="..\portcls\nn-portcls-iservicegroup.md">IServiceGroup</a>
</dt>
<dt>
<a href="..\portcls\nn-portcls-iservicesink.md">IServiceSink</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536918">IPortWavePci::Notify</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IMiniportWavePci::Service method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

