---
description: Константы, используемые для задания приоритета ресурса в SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273729"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="6e1af-103">\_Приоритет ресурса \_ d3d9</span><span class="sxs-lookup"><span data-stu-id="6e1af-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="6e1af-104">Константы, используемые для задания приоритета ресурса в [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span><span class="sxs-lookup"><span data-stu-id="6e1af-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="6e1af-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="6e1af-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="6e1af-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6e1af-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="6e1af-107"><dt>**D3d9 \_ \_ \_ Минимальный приоритет ресурса**</dt> <dt>0x28000000</dt></span><span class="sxs-lookup"><span data-stu-id="6e1af-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="6e1af-108">Ресурс имеет самый низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="6e1af-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="6e1af-109">Эта константа помечает ресурс как неиспользуемый и для вытеснения.</span><span class="sxs-lookup"><span data-stu-id="6e1af-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="6e1af-110">Ресурс должен быть исключен, как только другой ресурс требует объем памяти, занимаемый ресурсом.</span><span class="sxs-lookup"><span data-stu-id="6e1af-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="6e1af-111"><dt>**D3d9 \_ \_Приоритет ресурсов \_ низкая**</dt> <dt>0x50000000</dt></span><span class="sxs-lookup"><span data-stu-id="6e1af-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="6e1af-112">Ресурс запланирован с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6e1af-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="6e1af-113">Размещение ресурса не является критическим, и операционная система выполняет минимальную работу, чтобы найти расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6e1af-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="6e1af-114">Пометка ресурса как низкого приоритета позволяет другим более важным ресурсам занимать более быструю память.</span><span class="sxs-lookup"><span data-stu-id="6e1af-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="6e1af-115"><dt>**D3d9 \_ Приоритет ресурса — \_ \_ Обычная**</dt> <dt>0x78000000</dt></span><span class="sxs-lookup"><span data-stu-id="6e1af-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="6e1af-116">Ресурс запланирован с нормальным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6e1af-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="6e1af-117">Расположение ресурса важно для повышения производительности, но это не очень важно.</span><span class="sxs-lookup"><span data-stu-id="6e1af-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="6e1af-118">Операционная система должна попытаться поместить ресурс, помеченный как нормальный, в предпочтительное расположение ресурса вместо ресурса с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6e1af-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="6e1af-119">Как правило, текстуры помечаются как обычные.</span><span class="sxs-lookup"><span data-stu-id="6e1af-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="6e1af-120"><dt>**D3d9 \_ Приоритет ресурсов — \_ \_ высокий**</dt> <dt>0xA0000000</dt></span><span class="sxs-lookup"><span data-stu-id="6e1af-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="6e1af-121">Ресурс запланирован с высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6e1af-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="6e1af-122">Размещение ресурса является критически важным для производительности.</span><span class="sxs-lookup"><span data-stu-id="6e1af-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="6e1af-123">Операционная система всегда пытается поместить ресурс, помеченный как высокий, в предпочтительное расположение ресурса вместо ресурса с низким приоритетом или с обычным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6e1af-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="6e1af-124">Как правило, целевые объекты рендеринга помечены как высокие.</span><span class="sxs-lookup"><span data-stu-id="6e1af-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="6e1af-125"><dt>**D3d9 \_ \_ \_ Максимальный приоритет ресурса**</dt> <dt>0xc8000000</dt></span><span class="sxs-lookup"><span data-stu-id="6e1af-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="6e1af-126">Ресурс имеет максимально возможный приоритет.</span><span class="sxs-lookup"><span data-stu-id="6e1af-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="6e1af-127">Эта константа помечает приоритет ресурса как Soft-закрепленный.</span><span class="sxs-lookup"><span data-stu-id="6e1af-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="6e1af-128">Кратковременно закрепленный ресурс удаляется из памяти, только если отсутствует другой способ разрешения памяти буфера DMA.</span><span class="sxs-lookup"><span data-stu-id="6e1af-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="6e1af-129">Операционная система пытается разделить буфер DMA до минимального размера и исключить все другие ресурсы, которые не закреплены и не закреплены, прежде чем будет удалено программно закрепленный ресурс.</span><span class="sxs-lookup"><span data-stu-id="6e1af-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="6e1af-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e1af-130">Remarks</span></span>

<span data-ttu-id="6e1af-131">Значения, отличные **от \_ d3d9 \_ \_ минимального приоритета ресурса** и **d3d9 \_ \_ приоритета \_ ресурсов** , рассматриваются планировщиком как указания.</span><span class="sxs-lookup"><span data-stu-id="6e1af-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="6e1af-132">Можно использовать уровни приоритета, отличные от значений, определенных ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6e1af-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="6e1af-133">Например, пометка ресурса с уровнем приоритета 0x78000001 указывает, что приоритет ресурса немного выше среднего.</span><span class="sxs-lookup"><span data-stu-id="6e1af-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1af-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6e1af-134">Requirements</span></span>



| <span data-ttu-id="6e1af-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6e1af-135">Requirement</span></span> | <span data-ttu-id="6e1af-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6e1af-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1af-137">Header</span><span class="sxs-lookup"><span data-stu-id="6e1af-137">Header</span></span><br/> | <dl> <span data-ttu-id="6e1af-138"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e1af-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1af-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e1af-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1af-140">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="6e1af-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
