---
description: Содержит данные для отчетов о нехватке памяти.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Структура D3DMEMORYPRESSURE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713755"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="debcf-103">Структура D3DMEMORYPRESSURE (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="debcf-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="debcf-104">Содержит данные для отчетов о нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="debcf-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="debcf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="debcf-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="debcf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="debcf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="debcf-107">**битесевиктедфромпроцесс**</span><span class="sxs-lookup"><span data-stu-id="debcf-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="debcf-108">Тип: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="debcf-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="debcf-109">Число байтов, которые были исключены процессом во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="debcf-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="debcf-110">**сизеофинеффиЦиенталлокатион**</span><span class="sxs-lookup"><span data-stu-id="debcf-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="debcf-111">Тип: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="debcf-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="debcf-112">Общее число байтов, помещенных в неоптимальные сегменты памяти из-за недостаточного места в предпочтительных сегментах памяти.</span><span class="sxs-lookup"><span data-stu-id="debcf-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="debcf-113">**левелофеффиЦиенци**</span><span class="sxs-lookup"><span data-stu-id="debcf-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="debcf-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="debcf-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="debcf-115">Общая эффективность выделения памяти, помещенных в неоптимальную память.</span><span class="sxs-lookup"><span data-stu-id="debcf-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="debcf-116">Значение выражается в процентах.</span><span class="sxs-lookup"><span data-stu-id="debcf-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="debcf-117">Например, значение 95 указывает, что выделения, помещаемые в непредпочтительные сегменты памяти, имеют эффективность 95%.</span><span class="sxs-lookup"><span data-stu-id="debcf-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="debcf-118">Это число не должно считаться точным измерением.</span><span class="sxs-lookup"><span data-stu-id="debcf-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="debcf-119">Требования</span><span class="sxs-lookup"><span data-stu-id="debcf-119">Requirements</span></span>



| <span data-ttu-id="debcf-120">Требование</span><span class="sxs-lookup"><span data-stu-id="debcf-120">Requirement</span></span> | <span data-ttu-id="debcf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="debcf-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="debcf-122">Header</span><span class="sxs-lookup"><span data-stu-id="debcf-122">Header</span></span><br/> | <dl> <span data-ttu-id="debcf-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="debcf-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="debcf-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="debcf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="debcf-125">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="debcf-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
