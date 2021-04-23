---
description: Эта структура содержит данные для отчетов о нехватке памяти.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Структура D3DMEMORYPRESSURE (D3d9types. h) для Microsoft Media Foundation
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
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188029"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a><span data-ttu-id="7dc5f-103">Структура D3DMEMORYPRESSURE (D3d9types. h) для Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7dc5f-103">D3DMEMORYPRESSURE structure (D3d9types.h) for Microsoft Media Foundation</span></span>

<span data-ttu-id="7dc5f-104">Содержит данные для отчетов о нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dc5f-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="7dc5f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7dc5f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dc5f-107">**битесевиктедфромпроцесс**</span><span class="sxs-lookup"><span data-stu-id="7dc5f-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="7dc5f-108">Число байтов, которые были исключены процессом во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="7dc5f-109">**сизеофинеффиЦиенталлокатион**</span><span class="sxs-lookup"><span data-stu-id="7dc5f-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="7dc5f-110">Общее число байтов, помещенных в неоптимальные сегменты памяти из-за недостаточного места в предпочтительных сегментах памяти.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="7dc5f-111">**левелофеффиЦиенци**</span><span class="sxs-lookup"><span data-stu-id="7dc5f-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="7dc5f-112">Общая эффективность выделения памяти, помещенных в неоптимальную память.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="7dc5f-113">Значение выражается в процентах.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="7dc5f-114">Например, значение 95 указывает, что выделения, помещаемые в непредпочтительные сегменты памяти, имеют эффективность 95%.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="7dc5f-115">Это число не должно считаться точным измерением.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dc5f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7dc5f-116">Requirements</span></span>



| <span data-ttu-id="7dc5f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7dc5f-117">Requirement</span></span> | <span data-ttu-id="7dc5f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7dc5f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc5f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dc5f-119">Minimum supported client</span></span> | <span data-ttu-id="7dc5f-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7dc5f-120">Windows 7 \[desktop apps only\]</span></span>                                                              |
| <span data-ttu-id="7dc5f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dc5f-121">Minimum supported server</span></span> | <span data-ttu-id="7dc5f-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7dc5f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span>                                                 |
| <span data-ttu-id="7dc5f-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7dc5f-123">Header</span></span>                  | <span data-ttu-id="7dc5f-124">D3d9types. h (включение D3d9. h)</span><span class="sxs-lookup"><span data-stu-id="7dc5f-124">D3d9types.h (include D3d9.h)</span></span> |



## <a name="see-also"></a><span data-ttu-id="7dc5f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dc5f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc5f-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="7dc5f-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="7dc5f-127">Отчеты о нехватке памяти</span><span class="sxs-lookup"><span data-stu-id="7dc5f-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




