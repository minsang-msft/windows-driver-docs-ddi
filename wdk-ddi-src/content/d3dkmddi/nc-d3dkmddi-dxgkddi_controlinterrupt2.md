---
UID: NC:d3dkmddi.DXGKDDI_CONTROLINTERRUPT2
title: DXGKDDI_CONTROLINTERRUPT2 (d3dkmddi.h)
description: Learn more about the DxgkDdi_ControlInterrupt2 function.
ms.date: 06/09/2023
ms.keywords: DXGKDDI_CONTROLINTERRUPT2, DXGKDDI_CONTROLINTERRUPT2 callback, DxgkDdi_ControlInterrupt2, DxgkDdi_ControlInterrupt2 callback function [Display Devices], d3dkmddi/DxgkDdi_ControlInterrupt2, display.dxgkddicontrolinterrupt2
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - DXGKDDI_CONTROLINTERRUPT2
 - d3dkmddi/DXGKDDI_CONTROLINTERRUPT2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3dkmddi.h
api_name:
 - DXGKDDI_CONTROLINTERRUPT2
product:
 - Windows
---

# DXGKDDI_CONTROLINTERRUPT2 callback function

## -description

The **DxgkDdi_ControlInterrupt2** function enables or disables the given interrupt type on the graphics hardware.

## -parameters

### -param hAdapter [in]

A handle to the adapter object for the graphics processing unit (GPU). The driver returned this handle in the *MiniportDeviceContext* parameter from a call to its [**DxgkDdiAddDevice**](../dispmprt/nc-dispmprt-dxgkddi_add_device.md) function.

### -param InterruptControl [in]

A [**DXGKARG_CONTROLINTERRUPT2**](./ns-d3dkmddi-_dxgkarg_controlinterrupt2.md) structure that supplies the interrupt type, as well as the VSYNC state.

## -returns

*DxgkDdi_ControlInterrupt2* returns one of the following values:

| **Return code** | **Description** |
|:--|:--|
| **STATUS_SUCCESS** | The interrupt type was successfully enabled or disabled on the graphics hardware. |
| **STATUS_NOT_IMPLEMENTED** | *DxgkDdi_ControlInterrupt2* does not support enabling or disabling the specified interrupt type. |

## -remarks

Only one of **DxgkDdiControlInterrupt2** or [**DxgkDdi_ControlInterrupt3**](./nc-d3dkmddi-dxgkddi_controlinterrupt3.md) will be used by the OS during the lifetime of an adapter.

WDDM 2.7 drivers that do not implement [**DxgkDdi_ControlInterrupt3**](./nc-d3dkmddi-dxgkddi_controlinterrupt3.md) are opting out of independent VidPn VSync control, and the OS will only call **DxgkDdi_ControlInterrupt2**. The [**DXGK_DRIVERCAPS**](./ns-d3dkmddi-_dxgk_drivercaps.md)**->IndependentVidPnVSync** capability must be 0 in drivers that do not support **DxgkDdi_ControlInterrupt3**; otherwise, the OS will fail adapter initialization. If driver does implement **DxgkDdi_ControlInterrupt3**, then the capability can be set to 0 or 1 to indicate Per-VidPn support.

## -see-also

[**DXGK_DRIVERCAPS**](./ns-d3dkmddi-_dxgk_drivercaps.md)

[**DXGKARG_CONTROLINTERRUPT2**](./ns-d3dkmddi-_dxgkarg_controlinterrupt2.md)

[**DXGKARG_CONTROLINTERRUPT3**](ns-d3dkmddi-dxgkarg_controlinterrupt3.md)

[**DxgkDdi_ControlInterrupt3**](./nc-d3dkmddi-dxgkddi_controlinterrupt3.md)

[**DxgkDdiAddDevice**](../dispmprt/nc-dispmprt-dxgkddi_add_device.md)
