---
description: Указывает, что набор инструкций D3DX в настоящее время оптимизирован для.
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: Перечисление D3DX_CPU_OPTIMIZATION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 208422604e79b3ef7a87b548e7d71eceedd9fb78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713581"
---
# <a name="d3dx_cpu_optimization-enumeration"></a><span data-ttu-id="3542f-103">\_ \_ Перечисление оптимизации ЦП D3DX</span><span class="sxs-lookup"><span data-stu-id="3542f-103">D3DX\_CPU\_OPTIMIZATION enumeration</span></span>

<span data-ttu-id="3542f-104">Указывает, что набор инструкций D3DX в настоящее время оптимизирован для.</span><span class="sxs-lookup"><span data-stu-id="3542f-104">Specifies the instruction set D3DX is currently optimized for.</span></span>

## <a name="syntax"></a><span data-ttu-id="3542f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3542f-105">Syntax</span></span>


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a><span data-ttu-id="3542f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="3542f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3542f-107"><span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ не \_ оптимизирован**</span><span class="sxs-lookup"><span data-stu-id="3542f-107"><span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX\_NOT\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="3542f-108">Не Оптимизируйте.</span><span class="sxs-lookup"><span data-stu-id="3542f-108">Do not optimize.</span></span>

</dd> <dt>

<span data-ttu-id="3542f-109"><span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNOW \_ оптимизирован**</span><span class="sxs-lookup"><span data-stu-id="3542f-109"><span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX\_3DNOW\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="3542f-110">Оптимизировать для 3DNow!</span><span class="sxs-lookup"><span data-stu-id="3542f-110">Optimize for a 3DNow!</span></span> <span data-ttu-id="3542f-111">набор инструкций.</span><span class="sxs-lookup"><span data-stu-id="3542f-111">instruction set.</span></span>

</dd> <dt>

<span data-ttu-id="3542f-112"><span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ оптимизирован**</span><span class="sxs-lookup"><span data-stu-id="3542f-112"><span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX\_SSE2\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="3542f-113">Оптимизировать для набора инструкций SSE2.</span><span class="sxs-lookup"><span data-stu-id="3542f-113">Optimize for an SSE2 instruction set.</span></span>

</dd> <dt>

<span data-ttu-id="3542f-114"><span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ SSE \_ оптимизирован**</span><span class="sxs-lookup"><span data-stu-id="3542f-114"><span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX\_SSE\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="3542f-115">Оптимизируйте для набора инструкций SSE.</span><span class="sxs-lookup"><span data-stu-id="3542f-115">Optimize for an SSE instruction set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3542f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3542f-116">Requirements</span></span>



| <span data-ttu-id="3542f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3542f-117">Requirement</span></span> | <span data-ttu-id="3542f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3542f-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3542f-119">Header</span><span class="sxs-lookup"><span data-stu-id="3542f-119">Header</span></span><br/> | <dl> <span data-ttu-id="3542f-120"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3542f-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3542f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3542f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3542f-122">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="3542f-122">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




