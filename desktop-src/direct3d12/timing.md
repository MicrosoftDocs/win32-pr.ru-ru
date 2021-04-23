---
title: Время (графика Direct3D 12)
description: В этом разделе рассматриваются запросы к отметкам времени и калибровка GPU и счетчиков времени ЦП.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2020
ms.locfileid: "104549041"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="738e4-103">Время (графика Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="738e4-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="738e4-104">В этом разделе рассматриваются запросы к отметкам времени и калибровка GPU и счетчиков времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="738e4-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="738e4-105">Периодичность метки времени</span><span class="sxs-lookup"><span data-stu-id="738e4-105">Timestamp frequency</span></span>

<span data-ttu-id="738e4-106">Приложение может запрашивать частоту меток времени GPU для отдельных команд в очереди (см. метод [**ID3D12CommandQueue:: жеттиместампфрекуенци**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).</span><span class="sxs-lookup"><span data-stu-id="738e4-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="738e4-107">Возвращаемая частота измеряется в Гц (тактов/с).</span><span class="sxs-lookup"><span data-stu-id="738e4-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="738e4-108">Если указанная очередь команд не поддерживает метки времени (см. таблицу в разделе [запросов](queries.md) ), то этот API завершается с ошибкой (и возвращает **E_FAIL**).</span><span class="sxs-lookup"><span data-stu-id="738e4-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="738e4-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) и [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) всегда поддерживают метки времени.</span><span class="sxs-lookup"><span data-stu-id="738e4-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="738e4-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) также поддерживает метки времени, если член [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: Копикуеуетиместампкуериессуппортед**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="738e4-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="738e4-111">Калибровка метки времени</span><span class="sxs-lookup"><span data-stu-id="738e4-111">Timestamp calibration</span></span>

<span data-ttu-id="738e4-112">D3D12 позволяет приложениям сопоставлять результаты, полученные из запросов меток времени, с результатами, полученными от вызова `QueryPerformanceCounter` .</span><span class="sxs-lookup"><span data-stu-id="738e4-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="738e4-113">Это можно включить с помощью вызова [**ID3D12CommandQueue:: жетклокккалибратион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span><span class="sxs-lookup"><span data-stu-id="738e4-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="738e4-114">[**Жетклокккалибратион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) пример счетчика метки времени GPU для заданной очереди команд и одновременное выборка счетчика ЦП `QueryPerformanceCounter` с помощью.</span><span class="sxs-lookup"><span data-stu-id="738e4-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="738e4-115">\_Если указанная очередь команд не поддерживает метки времени, то этот API завершается ошибкой (возвращается значение E fail) (см. таблицу в разделе [запросов](queries.md) ).</span><span class="sxs-lookup"><span data-stu-id="738e4-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="738e4-116">Обратите внимание, что счетчики времени GPU и ЦП не обязательно напрямую связаны с тактовой частотой этих процессоров, а работают с квантами времени.</span><span class="sxs-lookup"><span data-stu-id="738e4-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="738e4-117">Запросы меток времени</span><span class="sxs-lookup"><span data-stu-id="738e4-117">Timestamp queries</span></span>

<span data-ttu-id="738e4-118">Метки времени можно получить как часть списка команд (а не вызова на стороне процессора в очереди команд) с помощью запросов отметок времени.</span><span class="sxs-lookup"><span data-stu-id="738e4-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="738e4-119">(Общие сведения о запросах см. в разделе [запросы](queries.md) .)</span><span class="sxs-lookup"><span data-stu-id="738e4-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="738e4-120">Все запросы timestamp используют тип [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) для фактического запроса.</span><span class="sxs-lookup"><span data-stu-id="738e4-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="738e4-121">Однако из-за ограничений, связанных с оборудованием, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) и [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) используют разные [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) , которые [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) использовать.</span><span class="sxs-lookup"><span data-stu-id="738e4-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="738e4-122">В очередях Direct и COMPUTE используются [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="738e4-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="738e4-123">Очереди копирования используют [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="738e4-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="738e4-124">Запросы очереди копирования поддерживаются только в том случае, если элемент [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: копикуеуетиместампкуериессуппортед**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="738e4-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="738e4-125">Запросы отметок времени после разрешения через [**ID3D12GraphicsCommandList:: ресолвекуеридата**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)являются **UINT64** , представляющими такты, как возвращаемые [**ID3D12CommandQueue:: жетклокккалибратион**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), и поэтому его необходимо разделить частотой очереди для получения длины в секундах.</span><span class="sxs-lookup"><span data-stu-id="738e4-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="738e4-126">Для точности используйте арифметические операции с плавающей запятой при вычислении интервала времени в секундах или миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="738e4-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="738e4-127">Например, используйте `queriedTicks / (double)Frequency` вместо `queriedTicks / Frequency`.</span><span class="sxs-lookup"><span data-stu-id="738e4-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="738e4-128">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="738e4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="738e4-129">Счетчики и запросы</span><span class="sxs-lookup"><span data-stu-id="738e4-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="738e4-130">**ID3D12Device:: Сетстаблеповерстате**</span><span class="sxs-lookup"><span data-stu-id="738e4-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="738e4-131">**ID3D12Object:: SetName**</span><span class="sxs-lookup"><span data-stu-id="738e4-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="738e4-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="738e4-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="738e4-133">Измерение производительности</span><span class="sxs-lookup"><span data-stu-id="738e4-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>
