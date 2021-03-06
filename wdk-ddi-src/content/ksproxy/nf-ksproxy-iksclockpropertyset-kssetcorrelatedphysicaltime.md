---
UID: NF:ksproxy.IKsClockPropertySet.KsSetCorrelatedPhysicalTime
title: IKsClockPropertySet::KsSetCorrelatedPhysicalTime method
author: windows-driver-content
description: The KsSetCorrelatedPhysicalTime method sets the physical time with the correlated system time on the underlying clock.
old-location: stream\iksclockpropertyset_kssetcorrelatedphysicaltime.htm
old-project: stream
ms.assetid: 208fecc5-f01f-41f3-80d3-d811b3f4173a
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: IKsClockPropertySet, IKsClockPropertySet::KsSetCorrelatedPhysicalTime, KsSetCorrelatedPhysicalTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ksproxy.h
req.include-header: Ksproxy.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IKsClockPropertySet.KsSetCorrelatedPhysicalTime
req.alt-loc: ksproxy.h
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
req.typenames: PIPE_STATE
---

# IKsClockPropertySet::KsSetCorrelatedPhysicalTime method



## -description
The <b>KsSetCorrelatedPhysicalTime</b> method sets the physical time with the correlated system time on the underlying clock. 



## -syntax

````
HRESULT KsSetCorrelatedPhysicalTime(
  [in] KSCORRELATED_TIME *CorrelatedTime
);
````


## -parameters

### -param CorrelatedTime [in]

Pointer to a <a href="..\ks\ns-ks-kscorrelated_time.md">KSCORRELATED_TIME</a> structure that contains the physical clock time along with the correlated system time to which to set the underlying clock. 


## -returns
Returns NOERROR if successful; otherwise, returns an error code.


## -remarks
The proxy uses the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564461">KSPROPERTY_CLOCK_CORRELATEDPHYSICALTIME</a> property to set the correlated time. 


## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559733">IKsClockPropertySet::KsGetCorrelatedPhysicalTime</a>
</dt>
<dt>
<a href="..\ks\ns-ks-kscorrelated_time.md">KSCORRELATED_TIME</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564461">KSPROPERTY_CLOCK_CORRELATEDPHYSICALTIME</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20IKsClockPropertySet::KsSetCorrelatedPhysicalTime method%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

