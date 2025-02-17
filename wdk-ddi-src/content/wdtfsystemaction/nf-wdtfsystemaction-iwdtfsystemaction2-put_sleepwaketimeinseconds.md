---
UID: NF:wdtfsystemaction.IWDTFSystemAction2.put_SleepWakeTimeInSeconds
title: IWDTFSystemAction2::put_SleepWakeTimeInSeconds (wdtfsystemaction.h)
description: Sets or gets the time in seconds when the system will wake from the sleep state.
old-location: dtf\iwdtfsystemaction2_sleepwaketimeinseconds.htm
tech.root: dtf
ms.date: 04/04/2018
keywords: ["IWDTFSystemAction2::put_SleepWakeTimeInSeconds"]
ms.keywords: IWDTFSystemAction2 interface [Windows Device Testing Framework],SleepWakeTimeInSeconds property, IWDTFSystemAction2.SleepWakeTimeInSeconds, IWDTFSystemAction2.put_SleepWakeTimeInSeconds, IWDTFSystemAction2::SleepWakeTimeInSeconds, IWDTFSystemAction2::get_SleepWakeTimeInSeconds, IWDTFSystemAction2::put_SleepWakeTimeInSeconds, Microsoft.WDTF.IWDTFSystemAction2.SleepWakeTimeInSeconds, Microsoft::WDTF::IWDTFSystemAction2::SleepWakeTimeInSeconds, SleepWakeTimeInSeconds property [Windows Device Testing Framework], SleepWakeTimeInSeconds property [Windows Device Testing Framework],IWDTFSystemAction2 interface, dtf.iwdtfsystemaction2_sleepwaketimeinseconds, put_SleepWakeTimeInSeconds, wdtfsystemaction/IWDTFSystemAction2::SleepWakeTimeInSeconds, wdtfsystemaction/IWDTFSystemAction2::get_SleepWakeTimeInSeconds, wdtfsystemaction/IWDTFSystemAction2::put_SleepWakeTimeInSeconds
req.header: wdtfsystemaction.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFSystemAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFSystemAction.Interop.dll
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDTFSystemAction2::put_SleepWakeTimeInSeconds
 - wdtfsystemaction/IWDTFSystemAction2::put_SleepWakeTimeInSeconds
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WDTFSystemAction.Interop.dll
api_name:
 - IWDTFSystemAction2::put_SleepWakeTimeInSeconds
---

# IWDTFSystemAction2::put_SleepWakeTimeInSeconds

## -description

Gets or sets the time in seconds when the system will wake from the sleep state.

This property is read/write.

## -parameters

### -param  nWakeTimeInSeconds

The time in seconds when the system will wake from the sleep state.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdtfsystemaction/nn-wdtfsystemaction-iwdtfsystemaction2">IWDTFSystemAction2</a>

