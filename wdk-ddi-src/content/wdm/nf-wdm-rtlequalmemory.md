---
UID: NF:wdm.RtlEqualMemory
title: RtlEqualMemory macro (wdm.h)
description: The RtlEqualMemory routine compares two blocks of memory to determine whether the specified number of bytes are identical.
tech.root: kernel
ms.date: 03/07/2023
keywords: ["RtlEqualMemory macro"]
ms.keywords: RtlEqualMemory, RtlEqualMemory routine [Kernel-Mode Driver Architecture], k109_a75dfbc8-12af-4f95-9ba0-b7752b796e55.xml, kernel.rtlequalmemory, wdm/RtlEqualMemory
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Desktop
req.target-min-winverclnt:
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
req.irql: Any level (See Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - RtlEqualMemory
 - wdm/RtlEqualMemory
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdm.h
api_name:
 - RtlEqualMemory
---

## -description

The **RtlEqualMemory** routine compares two blocks of memory to determine whether the specified number of bytes are identical.

## -parameters

### -param Destination [in]

A pointer to a caller-allocated block of memory to compare.

### -param Source [in]

A pointer to a caller-allocated block of memory that is compared to the block of memory to which *Source1* points.

### -param Length [in]

Specifies the number of bytes to be compared.

## -syntax

```cpp
BOOL WINAPI
RtlEqualMemory(
   void*  Destination,
   void*  Source,
   size_t Length
);
```

## -returns

## -remarks

**RtlEqualMemory** begins the comparison with byte zero of each block.

**RtlEqualMemory** returns TRUE if Source1 and Source2 are equivalent; otherwise, it returns FALSE.

Callers of **RtlEqualMemory** can be running at any IRQL if both blocks of memory are resident.

## -see-also

[RtlCompareMemory](./nf-wdm-rtlcomparememory.md)