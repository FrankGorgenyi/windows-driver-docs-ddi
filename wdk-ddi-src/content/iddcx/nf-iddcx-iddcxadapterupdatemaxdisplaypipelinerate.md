---
UID: NF:iddcx.IddCxAdapterUpdateMaxDisplayPipelineRate
title: IddCxAdapterUpdateMaxDisplayPipelineRate function
author: windows-driver-content
description: An OS callback function the driver calls to report that the max display pipeline rate has changed.
old-location: display\iddcxadapterupdatemaxdisplaypipelinerate.htm
old-project: display
ms.assetid: 5d8e6b87-6cfd-48ec-ac38-a75cb94cf5ac
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: IddCxAdapterUpdateMaxDisplayPipelineRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iddcx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IddCxAdapterUpdateMaxDisplayPipelineRate
req.alt-loc: iddcx.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: _Must_inspect_result_
req.typenames: 
---

# IddCxAdapterUpdateMaxDisplayPipelineRate function



## -description


                An OS callback function the driver calls to report that the max display pipeline rate has changed



## -syntax

````
NTSTATUS IddCxAdapterUpdateMaxDisplayPipelineRate(
  _In_       IDDCX_ADAPTER                    hOsAdapterContext,
  _In_ const IDARG_IN_MAXDISPLAYPIPELINERATE* pInArgs
);
````


## -parameters

### -param hOsAdapterContext [in]

This is the OS context handle for this adapter returned by the <b>IddCxStart</b> call


### -param pInArgs [in]

Input arguments to the function


## -returns

(NTSTATUS) The method returns S_OK if the operation succeeds. Otherwise, this method may return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.
                    


## -remarks
