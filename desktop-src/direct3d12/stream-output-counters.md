---
title: Счетчики потокового вывода
description: Потоковая передача данных — это способность GPU записывать вершины в буфер. Счетчики потокового вывода отслеживают ход выполнения.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105099"
---
# <a name="stream-output-counters"></a><span data-ttu-id="9e73b-104">Счетчики потокового вывода</span><span class="sxs-lookup"><span data-stu-id="9e73b-104">Stream Output Counters</span></span>

<span data-ttu-id="9e73b-105">Потоковая передача данных — это способность GPU записывать вершины в буфер.</span><span class="sxs-lookup"><span data-stu-id="9e73b-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="9e73b-106">Счетчики потокового вывода отслеживают ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="9e73b-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="9e73b-107">Различия в потоковых счетчиках с Direct3D 11 до Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9e73b-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="9e73b-108">буфферфилледсизе</span><span class="sxs-lookup"><span data-stu-id="9e73b-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="9e73b-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9e73b-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="9e73b-110">Различия в потоковых счетчиках с Direct3D 11 до Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9e73b-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="9e73b-111">Как часть процесса потокового вывода, GPU должен изучить текущее расположение в буфере, в который он записывается.</span><span class="sxs-lookup"><span data-stu-id="9e73b-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="9e73b-112">В Direct3D 11 память для хранения этого расположения выделяется драйвером, и единственный способ управления этим значением — с помощью метода **сосеттаржетс** .</span><span class="sxs-lookup"><span data-stu-id="9e73b-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="9e73b-113">В Direct3D 12 приложения выделяют память для хранения текущего расположения.</span><span class="sxs-lookup"><span data-stu-id="9e73b-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="9e73b-114">Для работы с этим значением не существует специальных способов, и приложения могут считывать и записывать значение с помощью ЦП или GPU.</span><span class="sxs-lookup"><span data-stu-id="9e73b-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="9e73b-115">буфферфилледсизе</span><span class="sxs-lookup"><span data-stu-id="9e73b-115">BufferFilledSize</span></span>

<span data-ttu-id="9e73b-116">Приложение отвечает за выделение хранилища для 32-разрядного количества, именуемого *буфферфилледсизе*.</span><span class="sxs-lookup"><span data-stu-id="9e73b-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="9e73b-117">Содержит число байтов данных в буфере потока вывода.</span><span class="sxs-lookup"><span data-stu-id="9e73b-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="9e73b-118">Это хранилище можно разместить в том же или другом ресурсе, в котором содержатся выходные данные потока.</span><span class="sxs-lookup"><span data-stu-id="9e73b-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="9e73b-119">Доступ к этому значению осуществляется с помощью GPU на стадии потокового вывода, чтобы определить, куда добавлять новые данные вершин в буфер.</span><span class="sxs-lookup"><span data-stu-id="9e73b-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="9e73b-120">Кроме того, доступ к этому значению осуществляется с помощью графического процессора, чтобы определить, когда произошло переполнение.</span><span class="sxs-lookup"><span data-stu-id="9e73b-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="9e73b-121">См. структуру [**D3D12 \_ потока \_ OUTPUT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span><span class="sxs-lookup"><span data-stu-id="9e73b-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="9e73b-122">Слой отладки будет проверять следующее в [**ID3D12GraphicsCommandList:: сосеттаржетс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="9e73b-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="9e73b-123">*Буфферфилледсизе* попадает в диапазон, подразумеваемый {*оффсетинбитес*, *сизеинбитес*}, если указан ресурс, отличный от NULL.</span><span class="sxs-lookup"><span data-stu-id="9e73b-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="9e73b-124">*Буфферфилледсизеоффсетинбитес* является кратным 4.</span><span class="sxs-lookup"><span data-stu-id="9e73b-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="9e73b-125">*Буфферфилледсизеоффсетинбитес* находится в диапазоне содержащего ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e73b-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="9e73b-126">Указанный ресурс является буфером.</span><span class="sxs-lookup"><span data-stu-id="9e73b-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="9e73b-127">Среда выполнения не будет проверять тип кучи, связанный с выходным буфером потока, поскольку выходной поток поддерживается во всех типах кучи.</span><span class="sxs-lookup"><span data-stu-id="9e73b-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="9e73b-128">Корневые подписи должны указывать, будет ли использоваться выходной поток, используя флаги флагов [**\_ корневой \_ подписи \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .</span><span class="sxs-lookup"><span data-stu-id="9e73b-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="9e73b-129">\_Флаг корневой \_ подписи D3D12 \_ \_ позволяет \_ \_ указать выходные данные потока для корневых подписей, созданных в HLSL, так же, как и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="9e73b-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="9e73b-130">[**Креатеграфикспипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) завершится ошибкой, если шейдер геометрии содержит потоковый выход, но у корневой подписи нет \_ установленного флага корневой \_ сигнатуры D3D12 " \_ \_ Разрешить \_ выходной поток" \_ .</span><span class="sxs-lookup"><span data-stu-id="9e73b-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="9e73b-131">Если ресурс используется в качестве целевого объекта вывода потока, используемые ресурсы должны находиться в \_ состоянии D3D12 ресурсов \_ \_ потока состояния \_ .</span><span class="sxs-lookup"><span data-stu-id="9e73b-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="9e73b-132">Это относится как к данным вершин, так и к *буфферфилледсизе* (которые могут находиться в одном или разных ресурсах).</span><span class="sxs-lookup"><span data-stu-id="9e73b-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="9e73b-133">Нет специальных интерфейсов API для задания смещения буфера вывода потока, так как приложения могут записывать данные в *буфферфилледсизе* с помощью ЦП или GPU напрямую.</span><span class="sxs-lookup"><span data-stu-id="9e73b-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e73b-134">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9e73b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e73b-135">Счетчики и запросы</span><span class="sxs-lookup"><span data-stu-id="9e73b-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




