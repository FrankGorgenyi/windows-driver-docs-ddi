---
UID: NE:ntddndis._NDIS_PM_WAKE_REASON_TYPE
title: _NDIS_PM_WAKE_REASON_TYPE
author: windows-driver-content
description: The NDIS_PM_WAKE_REASON_TYPE enumeration identifies the type of wake-up event that was generated by the network adapter.
old-location: netvista\ndis_pm_wake_reason_type.htm
old-project: netvista
ms.assetid: 7919226a-4d36-4397-bca1-f7338b3e7ade
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: _NDIS_PM_WAKE_REASON_TYPE, *PNDIS_PM_WAKE_REASON_TYPE, NDIS_PM_WAKE_REASON_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddndis.h
req.include-header: Ntddndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.30 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: NDIS_PM_WAKE_REASON_TYPE
req.alt-loc: ntddndis.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.typenames: *PNDIS_PM_WAKE_REASON_TYPE, NDIS_PM_WAKE_REASON_TYPE
---

# _NDIS_PM_WAKE_REASON_TYPE enumeration



## -description

The <b>NDIS_PM_WAKE_REASON_TYPE</b> enumeration identifies the type of wake-up event that was generated by the network adapter.



The <b>NDIS_PM_WAKE_REASON_TYPE</b> enumeration identifies the type of wake-up event that was generated by the network adapter.



## -syntax

````
typedef enum _NDIS_PM_WAKE_REASON_TYPE { 
  NdisWakeReasonUnspecified               = 0x0000,
  NdisWakeReasonPacket                    = 0x0001,
  NdisWakeReasonMediaDisconnect           = 0x0002,
  NdisWakeReasonMediaConnect              = 0x0003,
  NdisWakeReasonWlanNLODiscovery          = 0x1000,
  NdisWakeReasonWlanAPAssociationLost     = 0x1001,
  NdisWakeReasonWlanGTKHandshakeError     = 0x1002,
  NdisWakeReasonWlan4WayHandshakeRequest  = 0x1003,
  NdisWakeReasonWwanRegisterState         = 0x2000,
  NdisWakeReasonWwanSMSReceive            = 0x2001,
  NdisWakeReasonWwanUSSDReceive           = 0x2002
} NDIS_PM_WAKE_REASON_TYPE, *PNDIS_PM_WAKE_REASON_TYPE;
````


## -enum-fields

### -field NdisWakeReasonUnspecified

The type of wake-up event is not specified.


### -field NdisWakeReasonPacket

The network adapter generated the wake-up event because it received a packet that matched a wake-on-LAN (WOL) pattern.


### -field NdisWakeReasonMediaDisconnect

The network adapter generated the wake-up event because it disconnected from the network media.


### -field NdisWakeReasonMediaConnect

The network adapter generated the wake-up event because it connected to the network media.


### -field NdisWakeReasonWlanNLODiscovery

The 802.11 network adapter generated the wake-up event because it detected a service set identifier (SSID) that was specified through a network list offload (NLO). 

For more information about NLO, see <a href="https://msdn.microsoft.com/528838AA-4002-4923-A71B-37ADEE9B8D07">Wi-Fi Network List Offload</a>.


### -field NdisWakeReasonWlanAPAssociationLost

The 802.11 network adapter generated the wake-up event because it became disassociated with the access point (AP).


### -field NdisWakeReasonWlanGTKHandshakeError

The 802.11 network adapter generated the wake-up event because it encountered an error during the IEEE 802.11i RSN group transient key (GTK) handshake with the AP.


### -field NdisWakeReasonWlan4WayHandshakeRequest

The 802.11 network adapter generated the wake-up event because it received the first frame of the IEEE 802.11i RSN 4-way handshake with the AP. This handshake is performed when the adapter authenticates with the AP.


### -field NdisWakeReasonWwanRegisterState

The mobile broadband (MB) network adapter generated the wake-up event because its registration state to the MB Service has changed.


### -field NdisWakeReasonWwanSMSReceive

The mobile broadband (MB) network adapter generated the wake-up event because the MB Service has to be notified about the receipt of a Short Message Service (SMS) message. The adapter generates this wake-up event either after the completion of a previously-issued <a href="https://msdn.microsoft.com/library/windows/hardware/ff569839">OID_WWAN_SMS_READ</a> query request, or the arrival of a new class-0 (flash/alert) message from the network provider as an event notification.


### -field NdisWakeReasonWwanUSSDReceive

The mobile broadband (MB) network adapter generated the wake-up event because it received an Unstructured Supplementary Service Data (USSD) message.


## -remarks
The  
    <b>WakeReason</b> member of the 
    <a href="..\ntddndis\ns-ntddndis-_ndis_pm_wake_reason.md">NDIS_PM_WAKE_REASON</a> structure contains an <b>NDIS_PM_WAKE_REASON_TYPE</b> enumeration value.


## -see-also
<dl>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_pm_wake_reason.md">NDIS_PM_WAKE_REASON</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_PM_WAKE_REASON_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

