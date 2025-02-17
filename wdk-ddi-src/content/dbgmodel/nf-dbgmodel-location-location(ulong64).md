---
UID: NF:dbgmodel.Location.Location(ULONG64)
title: Location(ULONG64) function (dbgmodel.h)
description: Constructs a location from an offset into the virtual address space of the target.
ms.date: 09/28/2018
keywords: ["Location function"]
ms.keywords: Location
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - Location::Location
 - dbgmodel/Location::Location
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dbgmodel.h
api_name:
 - Location::Location
---

# Location(ULONG64) function (dbgmodel.h)


## -description

Constructs a location from an offset into the virtual address space of the target.

## -parameters

### -param virtualAddress

The virtual address.

## -returns

This function is a constructor and does not return value.

## -remarks

Defines the location for an object.  This particular variant of Location is the C-COM access struct.
Note that a location only has meaning in conjunction with a host context.  It is a location within
a context.  When performing an operation on the location (reading bytes, writing bytes, etc...), a valid host context must be supplied.

### Returns

This function is a constructor and does not return value.


## -see-also

[dbgmodel.h header](./index.md)

