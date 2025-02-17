---
UID: NC:d3dkmddi.DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO
title: DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO (d3dkmddi.h)
description: The pfnReleasePathInfo function releases a D3DKMDT_VIDPN_PRESENT_PATH structure that the VidPN manager previously provided to the display miniport driver.
old-location: display\dxgk_vidpntopology_interface_pfnreleasepathinfo.htm
ms.date: 05/10/2018
keywords: ["DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO callback function"]
ms.keywords: DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO, DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO callback, VidPnFunctions_2bbba27c-cbbe-40ea-9ba6-0da2d7d237d5.xml, d3dkmddi/pfnReleasePathInfo, display.dxgk_vidpntopology_interface_pfnreleasepathinfo, pfnReleasePathInfo, pfnReleasePathInfo callback function [Display Devices]
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows Vista
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
 - DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO
 - d3dkmddi/DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3dkmddi.h
api_name:
 - DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO
product:
 - Windows
---

# DXGKDDI_VIDPNTOPOLOGY_RELEASEPATHINFO callback function


## -description

The <b>pfnReleasePathInfo</b> function releases a <a href="/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_d3dkmdt_vidpn_present_path">D3DKMDT_VIDPN_PRESENT_PATH</a> structure that the VidPN manager previously provided to the display miniport driver.

## -parameters

### -param hVidPnTopology [in]

A handle to a VidPN topology object. The display miniport driver previously obtained this handle by calling the <a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpn_gettopology">pfnGetTopology</a> function of the <a href="/windows-hardware/drivers/ddi/d3dkmddi/ns-d3dkmddi-_dxgk_vidpn_interface">DXGK_VIDPN_INTERFACE</a> interface.

### -param pVidPnPresentPathInfo [in]

A pointer to the D3DKMDT_VIDPN_PRESENT_PATH structure that is to be released.

## -returns

The <b>pfnReleasePathInfo</b> function returns one of the following values:

|Return code|Description|
|--- |--- |
|STATUS_SUCCESS|The function succeeded.|
|STATUS_GRAPHICS_INVALID_VIDPN_TOPOLOGY|The handle supplied in hVidPnTopology was invalid.|
|STATUS_GRAPHICS_INVALID_VIDPN_PRESENT_PATH|The pointer supplied in pVidPnPresentPathInfo was invalid.|

## -remarks

When you have finished using a D3DKMDT_VIDPN_PRESENT_PATH structure that you obtained by calling any of the following functions, you must release the structure by calling <b>pfnReleasePathInfo</b>.

<ul>
<li>

<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpntopology_acquirefirstpathinfo">pfnAcquireFirstPathInfo</a>


</li>
<li>

<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpntopology_acquirenextpathinfo">pfnAcquireNextPathInfo</a>


</li>
<li>

<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpntopology_acquirepathinfo">pfnAcqirePathInfo</a>


</li>
</ul>
If you obtain a D3DKMDT_VIDPN_PRESENT_PATH structure by calling <b><u>pfnCreateNewPathInfo</u></b> and then pass that structure to <b><u>pfnAddPath</u></b>, you do not need to release the structure.

If you obtain a handle by calling <b>pfnCreateNewPathInfo</b> and then you decide not to add the new path to a topology, you must release the newly created structire by calling <b>pfnReleasePathInfo</b>.

The D3DKMDT_HVIDPNTOPOLOGY data type is defined in <i>D3dkmdt.h</i>.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_d3dkmdt_vidpn_present_path">D3DKMDT_VIDPN_PRESENT_PATH</a>



<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpntopology_acquirepathinfo">pfnAcqirePathInfo</a>



<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpntopology_acquirefirstpathinfo">pfnAcquireFirstPathInfo</a>



<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkddi_vidpntopology_acquirenextpathinfo">pfnAcquireNextPathInfo</a>

