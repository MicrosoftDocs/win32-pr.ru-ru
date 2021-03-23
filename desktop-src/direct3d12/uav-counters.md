---
title: Счетчики UAV
description: Счетчики неупорядоченного представления доступа (UAV) можно использовать для связывания 32-разрядного атомарного счетчика с неупорядоченным представлением доступа (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548961"
---
# <a name="uav-counters"></a><span data-ttu-id="326f2-103">Счетчики UAV</span><span class="sxs-lookup"><span data-stu-id="326f2-103">UAV Counters</span></span>
<span data-ttu-id="326f2-104">Счетчики неупорядоченного представления доступа (UAV) можно использовать для связывания 32-разрядного атомарного счетчика с неупорядоченным представлением доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="326f2-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="326f2-105">Различия в счетчиках UAV с Direct3D 11 до Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="326f2-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="326f2-106">Приложения Direct3D 12 и Direct3D 11 используют одни и те же функции шейдера высокого уровня шейдеров (HLSL) для доступа к счетчикам UAV.</span><span class="sxs-lookup"><span data-stu-id="326f2-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="326f2-107">**инкременткаунтер**</span><span class="sxs-lookup"><span data-stu-id="326f2-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="326f2-108">**декременткаунтер**</span><span class="sxs-lookup"><span data-stu-id="326f2-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="326f2-109">**Добавить**</span><span class="sxs-lookup"><span data-stu-id="326f2-109">**Append**</span></span>
-   <span data-ttu-id="326f2-110">**Использование**</span><span class="sxs-lookup"><span data-stu-id="326f2-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="326f2-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="326f2-111">Direct3D 12</span></span>
<span data-ttu-id="326f2-112">В Direct3D 12 32-битные значения выделяются приложением, поэтому 32-разрядные значения могут быть считаны и записаны либо ЦП, либо GPU, как и любой другой ресурс Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="326f2-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="326f2-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="326f2-113">Direct3D 11</span></span>
<span data-ttu-id="326f2-114">За пределами шейдеров с помощью Direct3D 11 необходимо вызывать методы API для доступа к счетчикам (например, [ссылку ID3D11DeviceContext:: копиструктурекаунт](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span><span class="sxs-lookup"><span data-stu-id="326f2-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="326f2-115">Использование счетчиков UAV</span><span class="sxs-lookup"><span data-stu-id="326f2-115">Using UAV counters</span></span>
<span data-ttu-id="326f2-116">Приложение отвечает за выделение 32-разрядов хранилища для счетчиков UAV.</span><span class="sxs-lookup"><span data-stu-id="326f2-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="326f2-117">Это хранилище можно выделить в другом ресурсе, который содержит данные, доступные через UAV.</span><span class="sxs-lookup"><span data-stu-id="326f2-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="326f2-118">См. [**креатеунордередакцессвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) и [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span><span class="sxs-lookup"><span data-stu-id="326f2-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="326f2-119">Если в вызове [**креатеунордередакцессвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)указан *пкаунтерресаурце* , то существует счетчик, связанный с UAV.</span><span class="sxs-lookup"><span data-stu-id="326f2-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="326f2-120">В данном случае:</span><span class="sxs-lookup"><span data-stu-id="326f2-120">In this case:</span></span>

-   <span data-ttu-id="326f2-121">*Структуребитестриде* должно быть больше нуля</span><span class="sxs-lookup"><span data-stu-id="326f2-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="326f2-122">Формат должен быть \_ \_ неизвестным в формате DXGI</span><span class="sxs-lookup"><span data-stu-id="326f2-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="326f2-123">Не следует задавать флаг RAW</span><span class="sxs-lookup"><span data-stu-id="326f2-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="326f2-124">Оба ресурса должны быть буферами</span><span class="sxs-lookup"><span data-stu-id="326f2-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="326f2-125">*Каунтероффсетинбитес* должен быть кратен 4 байтам</span><span class="sxs-lookup"><span data-stu-id="326f2-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="326f2-126">*Каунтероффсетинбитес* должен находиться в диапазоне ресурса счетчика</span><span class="sxs-lookup"><span data-stu-id="326f2-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="326f2-127">*пдеск* не может иметь значение null</span><span class="sxs-lookup"><span data-stu-id="326f2-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="326f2-128">*предисходный код* не может иметь значение null</span><span class="sxs-lookup"><span data-stu-id="326f2-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="326f2-129">И обратите внимание на следующие случаи использования:</span><span class="sxs-lookup"><span data-stu-id="326f2-129">And note the following use cases:</span></span>

-   <span data-ttu-id="326f2-130">Если *пкаунтерресаурце* не указан, то *каунтероффсетинбитес* должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="326f2-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="326f2-131">Если флаг RAW установлен, то формат должен быть в формате DXGI \_ \_ R32 без \_ типов, а ресурс UAV должен быть буфером.</span><span class="sxs-lookup"><span data-stu-id="326f2-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="326f2-132">Если *пкаунтерресаурце* не задан, то *каунтероффсетинбитес* должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="326f2-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="326f2-133">Если флаг RAW не установлен и *структуребитестриде* = 0, то формат должен быть допустимым форматом UAV.</span><span class="sxs-lookup"><span data-stu-id="326f2-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="326f2-134">Direct3D 12 устраняет различие между Append и Counter Уавс (хотя различие по-прежнему существует в байтах HLSL).</span><span class="sxs-lookup"><span data-stu-id="326f2-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="326f2-135">Основная среда выполнения будет проверять эти ограничения в [**креатеунордередакцессвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="326f2-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="326f2-136">Во время рисования или диспетчеризации ресурс счетчика должен находиться в состоянии [**ресурса D3D12 \_ \_ \_ неупорядоченный \_ доступ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span><span class="sxs-lookup"><span data-stu-id="326f2-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="326f2-137">Кроме того, в рамках одного вызова рисования/отправки приложение не может получить доступ к одному и тому же 32-разрядному расположению памяти через два отдельных счетчика UAV.</span><span class="sxs-lookup"><span data-stu-id="326f2-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="326f2-138">Если обнаружен один из этих элементов, отладочный слой выдаст ошибки.</span><span class="sxs-lookup"><span data-stu-id="326f2-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="326f2-139">Методы "Сетунордередакцессвиевкаунтервалуе" и "Копиструктурекаунт" отсутствуют, так как приложения могут просто копировать данные в значение счетчика напрямую и обратно.</span><span class="sxs-lookup"><span data-stu-id="326f2-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="326f2-140">Поддерживается динамическое индексирование Уавс с счетчиками.</span><span class="sxs-lookup"><span data-stu-id="326f2-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="326f2-141">Если шейдер пытается получить доступ к счетчику UAV, у которого нет связанного счетчика, то отладочный слой выдаст предупреждение, и произойдет ошибка страницы GPU, из-за чего будет удалено устройство приложения.</span><span class="sxs-lookup"><span data-stu-id="326f2-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="326f2-142">Счетчики UAV поддерживаются во всех типах куч (по умолчанию, upload, реадбакк).</span><span class="sxs-lookup"><span data-stu-id="326f2-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="326f2-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="326f2-143">Related topics</span></span>

* [<span data-ttu-id="326f2-144">Счетчики и запросы</span><span class="sxs-lookup"><span data-stu-id="326f2-144">Counters and queries</span></span>](counters-and-queries.md)