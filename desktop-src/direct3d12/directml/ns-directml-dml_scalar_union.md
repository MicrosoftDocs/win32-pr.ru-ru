---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Объединение скалярных типов.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418080"
---
# <a name="dml_scalar_union-union-directmlh"></a><span data-ttu-id="06cf3-103">Объединение DML_SCALAR_UNION (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="06cf3-103">DML_SCALAR_UNION union (directml.h)</span></span>
<span data-ttu-id="06cf3-104">Объединение скалярных типов.</span><span class="sxs-lookup"><span data-stu-id="06cf3-104">A union of scalar types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06cf3-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="06cf3-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="06cf3-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="06cf3-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="06cf3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06cf3-107">Syntax</span></span>
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a><span data-ttu-id="06cf3-108">Участники</span><span class="sxs-lookup"><span data-stu-id="06cf3-108">Members</span></span>

`Bytes`

<span data-ttu-id="06cf3-109">8-байтовый массив.</span><span class="sxs-lookup"><span data-stu-id="06cf3-109">An 8-byte array.</span></span>


`Int8`

<span data-ttu-id="06cf3-110">8-битовое целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="06cf3-110">An 8-bit signed integer.</span></span>


`UInt8`

<span data-ttu-id="06cf3-111">8-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="06cf3-111">An 8-bit unsigned integer.</span></span>


`Int16`

<span data-ttu-id="06cf3-112">16-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="06cf3-112">A 16-bit signed integer.</span></span>


`UInt16`

<span data-ttu-id="06cf3-113">16-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="06cf3-113">A 16-bit unsigned integer.</span></span>


`Int32`

<span data-ttu-id="06cf3-114">32-разрядное знаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="06cf3-114">A 32-bit signed integer.</span></span>


`UInt32`

<span data-ttu-id="06cf3-115">32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="06cf3-115">A 32-bit unsigned integer.</span></span>


`Int64`

<span data-ttu-id="06cf3-116">64-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="06cf3-116">A 64-bit signed integer.</span></span>


`UInt64`

<span data-ttu-id="06cf3-117">64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="06cf3-117">A 64-bit unsigned integer.</span></span>


`Float32`

<span data-ttu-id="06cf3-118">Число с плавающей запятой одиночной точности.</span><span class="sxs-lookup"><span data-stu-id="06cf3-118">A single precision floating-point number.</span></span>


`Float64`

<span data-ttu-id="06cf3-119">Число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="06cf3-119">A double precision floating-point number.</span></span>



## <a name="requirements"></a><span data-ttu-id="06cf3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="06cf3-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="06cf3-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="06cf3-121">**Header**</span></span> | <span data-ttu-id="06cf3-122">директмл. h</span><span class="sxs-lookup"><span data-stu-id="06cf3-122">directml.h</span></span> |