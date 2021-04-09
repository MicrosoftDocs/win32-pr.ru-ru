---
description: Содержит данные для отчетов о нехватке памяти.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
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
ms.openlocfilehash: 6d92cad29bda795a9589dbe0c94863bd743505bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143150"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="3de35-103">Структура D3DMEMORYPRESSURE (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="3de35-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="3de35-104">Содержит данные для отчетов о нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="3de35-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3de35-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="3de35-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3de35-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3de35-107">**битесевиктедфромпроцесс**</span><span class="sxs-lookup"><span data-stu-id="3de35-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="3de35-108">Число байтов, которые были исключены процессом во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="3de35-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="3de35-109">**сизеофинеффиЦиенталлокатион**</span><span class="sxs-lookup"><span data-stu-id="3de35-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="3de35-110">Общее число байтов, помещенных в неоптимальные сегменты памяти из-за недостаточного места в предпочтительных сегментах памяти.</span><span class="sxs-lookup"><span data-stu-id="3de35-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="3de35-111">**левелофеффиЦиенци**</span><span class="sxs-lookup"><span data-stu-id="3de35-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="3de35-112">Общая эффективность выделения памяти, помещенных в неоптимальную память.</span><span class="sxs-lookup"><span data-stu-id="3de35-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="3de35-113">Значение выражается в процентах.</span><span class="sxs-lookup"><span data-stu-id="3de35-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="3de35-114">Например, значение 95 указывает, что выделения, помещаемые в непредпочтительные сегменты памяти, имеют эффективность 95%.</span><span class="sxs-lookup"><span data-stu-id="3de35-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="3de35-115">Это число не должно считаться точным измерением.</span><span class="sxs-lookup"><span data-stu-id="3de35-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3de35-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3de35-116">Requirements</span></span>



| <span data-ttu-id="3de35-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3de35-117">Requirement</span></span> | <span data-ttu-id="3de35-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3de35-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de35-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3de35-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3de35-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3de35-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3de35-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3de35-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3de35-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3de35-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3de35-123">Header</span><span class="sxs-lookup"><span data-stu-id="3de35-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de35-124"><dt>D3d9types. h (включение D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3de35-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de35-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3de35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de35-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="3de35-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="3de35-127">Отчеты о нехватке памяти</span><span class="sxs-lookup"><span data-stu-id="3de35-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




