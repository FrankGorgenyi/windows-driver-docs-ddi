---
UID: NF:ntddk.IoWritePartitionTable
title: IoWritePartitionTable function
author: windows-driver-content
description: The IoWritePartitionTable routine is obsolete and is provided only to support existing drivers.
old-location: storage\iowritepartitiontable.htm
old-project: storage
ms.assetid: 406508b2-7509-4d2b-ac22-63644eedcec0
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: IoWritePartitionTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IoWritePartitionTable
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
req.typenames: WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---

# IoWritePartitionTable function



## -description
The <b>IoWritePartitionTable</b> routine is <b>obsolete</b> and is provided only to support existing drivers. New drivers must use <a href="..\ntddk\nf-ntddk-iowritepartitiontableex.md">IoWritePartitionTableEx</a>.

<b>IoWritePartitionTable</b> writes partition tables from the entries in the partition list buffer for each partition on the disk represented by the given device object.



## -syntax

````
NTSTATUS FASTCALL IoWritePartitionTable(
  _In_ PDEVICE_OBJECT                   DeviceObject,
  _In_ ULONG                            SectorSize,
  _In_ ULONG                            SectorsPerTrack,
  _In_ ULONG                            NumberOfHeads,
  _In_ struct _DRIVE_LAYOUT_INFORMATION *PartitionBuffer
);
````


## -parameters

### -param DeviceObject [in]

Pointer to the device object representing the disk whose partition tables are to be written.


### -param SectorSize [in]

Specifies the size in bytes of sectors on the device.


### -param SectorsPerTrack [in]

Specifies the track size on the device.


### -param NumberOfHeads [in]

Specifies the number of tracks per cylinder.


### -param PartitionBuffer [in]

Pointer to the drive layout buffer that contains the partition list entries. For more detailed information see <a href="..\ntdddisk\ns-ntdddisk-_drive_layout_information.md">DRIVE_LAYOUT_INFORMATION</a>.


## -returns
<b>IoWritePartitionTablo</b> returns a status code of STATUS_SUCCESS if all writes were completed without error. In case of failure, the error codes returned by <b>IoWritePartitionTable</b> might include, but are not limited to, the following list:
<dl>
<dt><b>STATUS_DEVICE_NOT_READY</b></dt>
</dl>Indicates a failure read the correct disk geometry.
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>Indicates a failure to allocate necessary resources (for example, heap memory, IRPs, etc.).
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>Indicates that sector zero did not have the expected MBR disk signature.

 


## -remarks
<b>IoWritePartitionTable</b> must only be used by disk drivers. Other drivers should use the <a href="..\ntdddisk\ni-ntdddisk-ioctl_disk_set_drive_layout.md">IOCTL_DISK_SET_DRIVE_LAYOUT</a> disk I/O request instead.

<b>IoWritePartitionTable</b> is called when a disk device driver is requested to set the partition type in a partition table entry or to repartition the disk by an IRP_MJ_DEVICE_CONTROL request. The device control request is generally issued by the format utility, which performs I/O control functions on the partitions and disks in the machine.

To reset a partition type, the driver passes a pointer to the device object representing the physical disk and the number of the partition associated with the device object that the format utility has open. When a disk is to be repartitioned dynamically, the disk driver must tear down its set of device objects representing the current disk partitions and create a new set of device objects representing the new partitions on the disk.

Applications that create and delete partitions and require full descriptions of the system should call <b>IoReadPartitionTable</b> with <i>ReturnRecognizedPartitions</i> set to <b>FALSE</b>. The drive layout structure can be modified by the system format utility to reflect a new configuration of the disk.

<b>IoWritePartitionTable</b> is synchronous. It must be called by the disk driver's Dispatch routine or by a driver thread. Thus, all user and file system threads must be prepared to enter a wait state when issuing the device control request to reset partition types for the device.


## -see-also
<dl>
<dt>
<a href="..\wdm\nf-wdm-iocreatedevice.md">IoCreateDevice</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-ioreadpartitiontable.md">IoReadPartitionTable</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-iosetpartitioninformation.md">IoSetPartitionInformation</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20IoWritePartitionTable routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

