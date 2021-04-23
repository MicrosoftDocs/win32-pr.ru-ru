---
description: Процент времени обработки данных в драйвере. Эти статистические данные могут помочь определить случаи, когда драйвер ожидает другие ресурсы.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Структура D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647837"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="9fdaa-104">\_Структура D3D9INTERFACETIMINGS D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="9fdaa-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="9fdaa-105">Процент времени обработки данных в драйвере.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="9fdaa-106">Эти статистические данные могут помочь определить случаи, когда драйвер ожидает другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fdaa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fdaa-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="9fdaa-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9fdaa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9fdaa-109">**ваитингфоргпутаусеаппликатионресаурцетимеперцент**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9fdaa-110">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9fdaa-111">Процент времени, затраченного драйвером на завершение работы GPU с заблокированным ресурсом (и [D3DLOCK \_ донотваит](d3dlock.md) не указан).</span><span class="sxs-lookup"><span data-stu-id="9fdaa-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="9fdaa-112">**ваитингфоргпутоакцептморекоммандстимеперцент**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9fdaa-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9fdaa-114">Процент времени, которое драйвер потратил на ожидание завершения обработки некоторых команд графическим процессором, прежде чем драйвер сможет отправить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="9fdaa-115">Это означает, что драйверу не хватает места для отправки команд GPU.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="9fdaa-116">**ваитингфоргпутостайвисинлатенцитимеперцент**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9fdaa-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9fdaa-118">Процент времени, затраченного драйвером на ожидание задержки GPU, чтобы сократить до трех кадров отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="9fdaa-119">Если приложение имеет ограниченный GPU, драйвер должен задержать его, пока GPU не выйдет из трех кадров.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="9fdaa-120">Это не позволяет приложению постановки в очередь вызовов отрисовки, которые могут значительно увеличить задержку между вводом пользователем новых данных, а также тем, когда пользователь видит результаты этого входа.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="9fdaa-121">Как правило, драйвер может отформатировать [**число вызовов,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) чтобы предотвратить постановку в очередь более трех кадров для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="9fdaa-122">**ваитингфоргпуексклусивересаурцетимеперцент**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9fdaa-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9fdaa-124">Процент времени, затраченного драйвером на ожидание ресурса, который не может быть конвейером (выполняется параллельно).</span><span class="sxs-lookup"><span data-stu-id="9fdaa-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="9fdaa-125">Приложение может захотеть избежать использования неконвейерного ресурса для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="9fdaa-126">**ваитингфоргпуосертимеперцент**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9fdaa-127">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9fdaa-128">Процент времени, затраченного драйвером на ожидание других операций обработки GPU.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fdaa-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fdaa-129">Remarks</span></span>

<span data-ttu-id="9fdaa-130">Эти метрики помогают определить время ожидания драйвера и его ожидание.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="9fdaa-131">Высокие проценты не обязательно являются проблемой.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="9fdaa-132">Эти глобальные метрики системы могут быть не реализованы.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="9fdaa-133">В зависимости от конкретного оборудования Эти метрики могут не поддерживать одновременно несколько запросов.</span><span class="sxs-lookup"><span data-stu-id="9fdaa-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fdaa-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9fdaa-134">Requirements</span></span>



| <span data-ttu-id="9fdaa-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9fdaa-135">Requirement</span></span> | <span data-ttu-id="9fdaa-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9fdaa-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdaa-137">Header</span><span class="sxs-lookup"><span data-stu-id="9fdaa-137">Header</span></span><br/> | <dl> <span data-ttu-id="9fdaa-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fdaa-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fdaa-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fdaa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fdaa-140">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9fdaa-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9fdaa-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="9fdaa-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
