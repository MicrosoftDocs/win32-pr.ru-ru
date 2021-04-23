---
title: Запросы затенения
description: В примере D3D12PredicationQueries демонстрируется отбор перекрытия с помощью куч запросов DirectX 12 и затенения. В этом пошаговом руководстве описывается дополнительный код, необходимый для расширения образца Хеллоконстбуффер для работы с запросами затенения.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad14e55864ee8d568acc0c9eb46134834d27ff54
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548919"
---
# <a name="predication-queries"></a><span data-ttu-id="0bf57-104">Запросы затенения</span><span class="sxs-lookup"><span data-stu-id="0bf57-104">Predication queries</span></span>

<span data-ttu-id="0bf57-105">В примере **D3D12PredicationQueries** демонстрируется отбор перекрытия с помощью куч запросов DirectX 12 и затенения.</span><span class="sxs-lookup"><span data-stu-id="0bf57-105">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="0bf57-106">В этом пошаговом руководстве описывается дополнительный код, необходимый для расширения образца **хеллоконстбуффер** для работы с запросами затенения.</span><span class="sxs-lookup"><span data-stu-id="0bf57-106">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span>

-   [<span data-ttu-id="0bf57-107">Создание кучи дескрипторов трафаретов глубины и кучи запросов перекрытия</span><span class="sxs-lookup"><span data-stu-id="0bf57-107">Create a depth stencil descriptor heap and an occlusion query heap</span></span>](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [<span data-ttu-id="0bf57-108">Включить альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="0bf57-108">Enable alpha blending</span></span>](#enable-alpha-blending)
-   [<span data-ttu-id="0bf57-109">Отключить записи цвета и глубины</span><span class="sxs-lookup"><span data-stu-id="0bf57-109">Disable color and depth writes</span></span>](#disable-color-and-depth-writes)
-   [<span data-ttu-id="0bf57-110">Создание буфера для хранения результатов запроса</span><span class="sxs-lookup"><span data-stu-id="0bf57-110">Create a buffer to store the results of the query</span></span>](#create-a-buffer-to-store-the-results-of-the-query)
-   [<span data-ttu-id="0bf57-111">Нарисуйте четыре и выполните и устраните запрос перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-111">Draw the quads and perform and resolve the occlusion query</span></span>](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [<span data-ttu-id="0bf57-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0bf57-112">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="0bf57-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0bf57-113">Related topics</span></span>](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a><span data-ttu-id="0bf57-114">Создание кучи дескрипторов трафаретов глубины и кучи запросов перекрытия</span><span class="sxs-lookup"><span data-stu-id="0bf57-114">Create a depth stencil descriptor heap and an occlusion query heap</span></span>

<span data-ttu-id="0bf57-115">В методе **лоадпипелине** создайте кучу дескрипторов шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="0bf57-115">In the **LoadPipeline** method create a depth stencil descriptor heap.</span></span>

``` syntax
              // Describe and create a depth stencil view (DSV) descriptor heap.
              D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
              dsvHeapDesc.NumDescriptors = 1;
              dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
              dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
              ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0bf57-116">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="0bf57-116">Call flow</span></span></th>
<th><span data-ttu-id="0bf57-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf57-117">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bf57-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="0bf57-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span></span><br />
<span data-ttu-id="0bf57-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_descriptor_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="0bf57-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>креатедескрипторхеап</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="0bf57-122">В методе **лоадассетс** создайте кучу для запросов перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-122">In the **LoadAssets** method create a heap for occlusion queries.</span></span>

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| <span data-ttu-id="0bf57-123">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="0bf57-123">Call flow</span></span>                                                 | <span data-ttu-id="0bf57-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf57-124">Parameters</span></span>                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="0bf57-125">**D3D12 \_ в \_ куче запросов \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0bf57-125">**D3D12\_QUERY\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [<span data-ttu-id="0bf57-126">**\_ \_ Тип КУЧИ запроса \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="0bf57-126">**D3D12\_QUERY\_HEAP\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [<span data-ttu-id="0bf57-127">**креатекуерихеап**</span><span class="sxs-lookup"><span data-stu-id="0bf57-127">**CreateQueryHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a><span data-ttu-id="0bf57-128">Включить альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="0bf57-128">Enable alpha blending</span></span>

<span data-ttu-id="0bf57-129">В этом примере соводятся два числа четырех и демонстрируется двоичный запрос перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-129">This sample draws two quads and illustrates a binary occlusion query.</span></span> <span data-ttu-id="0bf57-130">По экрану «четыре» на экране, а второй в обратном времени будет перекрыто.</span><span class="sxs-lookup"><span data-stu-id="0bf57-130">The quad in front animates across the screen, and the one in back will occasionally be occluded.</span></span> <span data-ttu-id="0bf57-131">В методе **лоадассетс** для этого образца включен альфа-смешение, чтобы мы могли увидеть, в какой точке D3D считает четыре из перекрыто.</span><span class="sxs-lookup"><span data-stu-id="0bf57-131">In the **LoadAssets** method, alpha blending is enabled for this sample so that we can see at what point D3D considers the quad in back occluded.</span></span>

``` syntax
     // Enable alpha blending so we can visualize the occlusion query results.
              CD3DX12_BLEND_DESC blendDesc(CD3DX12_DEFAULT);
              blendDesc.RenderTarget[0] =
              {
                     TRUE, FALSE,
                     D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_OP_ADD,
                     D3D12_BLEND_ONE, D3D12_BLEND_ZERO, D3D12_BLEND_OP_ADD,
                     D3D12_LOGIC_OP_NOOP,
                     D3D12_COLOR_WRITE_ENABLE_ALL,
              };
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0bf57-132">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="0bf57-132">Call flow</span></span></th>
<th><span data-ttu-id="0bf57-133">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf57-133">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bf57-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="0bf57-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span></span><br />
<span data-ttu-id="0bf57-136">[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_blend)</span><span class="sxs-lookup"><span data-stu-id="0bf57-136">[<strong>D3D12_BLEND</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)</span></span><br />
<span data-ttu-id="0bf57-137">[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_blend_op)</span><span class="sxs-lookup"><span data-stu-id="0bf57-137">[<strong>D3D12_BLEND_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)</span></span><br />
<span data-ttu-id="0bf57-138">[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_logic_op)</span><span class="sxs-lookup"><span data-stu-id="0bf57-138">[<strong>D3D12_LOGIC_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)</span></span><br />
<span data-ttu-id="0bf57-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_color_write_enable)</span><span class="sxs-lookup"><span data-stu-id="0bf57-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a><span data-ttu-id="0bf57-140">Отключить записи цвета и глубины</span><span class="sxs-lookup"><span data-stu-id="0bf57-140">Disable color and depth writes</span></span>

<span data-ttu-id="0bf57-141">Запрос перекрытия выполняется путем отрисовки четырех, охватывающих ту же область, что и «четыре», видимость которых мы хотим протестировать.</span><span class="sxs-lookup"><span data-stu-id="0bf57-141">The occlusion query is performed by rendering a quad that covers the same area as the quad whose visibility we want to test.</span></span> <span data-ttu-id="0bf57-142">В более сложных сценах запрос, скорее всего, будет ограниченным томом, а не простым из четырех.</span><span class="sxs-lookup"><span data-stu-id="0bf57-142">In more complex scenes, the query would likely be a bounding volume, rather than a simple quad.</span></span> <span data-ttu-id="0bf57-143">В любом случае создается новое состояние конвейера, которое отключает запись в целевой объект отрисовки и буфер z, чтобы сам запрос перекрытия не влиял на видимые выходные данные прохода отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0bf57-143">In either case, a new pipeline state is created that disables writing to the render target and the z buffer so that the occlusion query itself does not affect the visible output of the rendering pass.</span></span>

<span data-ttu-id="0bf57-144">В методе **лоадассетс** отключите записи цвета и записи глубины для состояния запроса перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-144">In the **LoadAssets** method, disable color writes and depth writes for the occlusion query's state.</span></span>

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| <span data-ttu-id="0bf57-145">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="0bf57-145">Call flow</span></span>                                                                            | <span data-ttu-id="0bf57-146">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf57-146">Parameters</span></span>                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="0bf57-147">**D3D12 \_ графика \_ состояния графического конвейера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bf57-147">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [<span data-ttu-id="0bf57-148">**\_ \_ Маска записи глубины \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="0bf57-148">**D3D12\_DEPTH\_WRITE\_MASK**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [<span data-ttu-id="0bf57-149">**креатеграфикспипелинестате**</span><span class="sxs-lookup"><span data-stu-id="0bf57-149">**CreateGraphicsPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a><span data-ttu-id="0bf57-150">Создание буфера для хранения результатов запроса</span><span class="sxs-lookup"><span data-stu-id="0bf57-150">Create a buffer to store the results of the query</span></span>

<span data-ttu-id="0bf57-151">В методе **лоадассетс** необходимо создать буфер для хранения результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="0bf57-151">In the **LoadAssets** method a buffer needs to be created to store the results of the query.</span></span> <span data-ttu-id="0bf57-152">Для каждого запроса требуется 8 байт свободного пространства в памяти GPU.</span><span class="sxs-lookup"><span data-stu-id="0bf57-152">Each query requires 8 bytes of space in GPU memory.</span></span> <span data-ttu-id="0bf57-153">В этом примере выполняется только один запрос, и простота и удобочитаемость создают буфер точно таким же размером (даже несмотря на то, что при вызове этой функции выделяется страница размером 64 КБ памяти GPU, большинство реальных приложений, скорее всего, будут создавать буфер большего размера).</span><span class="sxs-lookup"><span data-stu-id="0bf57-153">This sample only performs one query and for simplicity and readability creates a buffer exactly that size (even though this function call will allocate a 64K page of GPU memory - most real apps would likely create a larger buffer).</span></span>

``` syntax
 // Create the query result buffer.
              CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
              auto queryBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(8);
              ThrowIfFailed(m_device->CreateCommittedResource(
                     &heapProps,
                     D3D12_HEAP_FLAG_NONE,
                     &queryBufferDesc,
                     D3D12_RESOURCE_STATE_GENERIC_READ,
                     nullptr,
                     IID_PPV_ARGS(&m_queryResult)
                     ));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0bf57-154">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="0bf57-154">Call flow</span></span></th>
<th><span data-ttu-id="0bf57-155">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf57-155">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bf57-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>креатекоммиттедресаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="0bf57-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br />
<span data-ttu-id="0bf57-158">[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="0bf57-158">[<strong>D3D12_HEAP_TYPE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span></span><br />
<span data-ttu-id="0bf57-159">[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="0bf57-159">[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br />
<span data-ttu-id="0bf57-160">[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)</span><span class="sxs-lookup"><span data-stu-id="0bf57-160">[<strong>CD3DX12_RESOURCE_DESC</strong>](cd3dx12-resource-desc.md)</span></span><br />
<span data-ttu-id="0bf57-161">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="0bf57-161">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a><span data-ttu-id="0bf57-162">Нарисуйте четыре и выполните и устраните запрос перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-162">Draw the quads and perform and resolve the occlusion query</span></span>

<span data-ttu-id="0bf57-163">После завершения установки основной цикл обновляется в методе **популатекоммандлистс** .</span><span class="sxs-lookup"><span data-stu-id="0bf57-163">Having done the setup, the main loop is updated in the **PopulateCommandLists** method.</span></span>

<dl> 1. <span data-ttu-id="0bf57-164">Нарисуйте четыре эффекта, чтобы эффект прозрачности работал правильно.</span><span class="sxs-lookup"><span data-stu-id="0bf57-164">Draw the quads from back to front to make the transparency effect work properly.</span></span> <span data-ttu-id="0bf57-165">При рисовании «с конца на передний план» в результате запроса предыдущего кадра выдается предикат, который является довольно распространенным приемом.</span><span class="sxs-lookup"><span data-stu-id="0bf57-165">Drawing the quad in back to front is predicated on the result of the previous frame’s query and is a fairly common technique for this.</span></span>  
2. <span data-ttu-id="0bf57-166">Измените PSO, чтобы отключить целевой объект прорисовки и записи в трафарете глубины.</span><span class="sxs-lookup"><span data-stu-id="0bf57-166">Change the PSO to disable render target and depth stencil writes.</span></span>  
3. <span data-ttu-id="0bf57-167">Выполните запрос перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-167">Perform the occlusion query.</span></span>  
4. <span data-ttu-id="0bf57-168">Разрешите запрос перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0bf57-168">Resolve the occlusion query.</span></span>  
</dl>

``` syntax
       // Draw the quads and perform the occlusion query.
       {
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

              m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
              m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

              // Draw the far quad conditionally based on the result of the occlusion query
              // from the previous frame.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->DrawInstanced(4, 1, 0, 0);

              // Disable predication and always draw the near quad.
              m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
              m_commandList->DrawInstanced(4, 1, 4, 0);

              // Run the occlusion query with the bounding box quad.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPipelineState(m_queryState.Get());
              m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
              m_commandList->DrawInstanced(4, 1, 8, 0);
              m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

              // Resolve the occlusion query and store the results in the query result buffer
              // to be used on the subsequent frame.
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_COPY_DEST));
              m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_GENERIC_READ));
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0bf57-169">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="0bf57-169">Call flow</span></span></th>
<th><span data-ttu-id="0bf57-170">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf57-170">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bf57-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>жетгпудескрипторхандлефорхеапстарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>иасетпримитиветопологи</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>иасетвертексбуфферс</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>сетграфиксрутдескриптортабле</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>сетпредикатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>дравинстанцед</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>сетпредикатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>сетграфиксрутдескриптортабле</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>дравинстанцед</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>сетграфиксрутдескриптортабле</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>сетпипелинестате</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>бегинкуери</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>дравинстанцед</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>ендкуери</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ресаурцебарриер</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="0bf57-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="0bf57-193">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="0bf57-193">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bf57-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ресолвекуеридата</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span></span></td>
<td><span data-ttu-id="0bf57-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bf57-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ресаурцебарриер</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="0bf57-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bf57-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="0bf57-198">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/Ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="0bf57-198">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a><span data-ttu-id="0bf57-199">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0bf57-199">Run the sample</span></span>

<span data-ttu-id="0bf57-200">Не перекрыто:</span><span class="sxs-lookup"><span data-stu-id="0bf57-200">Not occluded:</span></span>

![два поля не перекрыто](images/not-occluded.png)

<span data-ttu-id="0bf57-202">Перекрыто</span><span class="sxs-lookup"><span data-stu-id="0bf57-202">Occluded:</span></span>

![одно поле полностью перекрыто](images/occluded.png)

<span data-ttu-id="0bf57-204">Частично перекрыто:</span><span class="sxs-lookup"><span data-stu-id="0bf57-204">Partially occluded:</span></span>

![один прямоугольник частично перекрыто](images/partially-occluded.png)

## <a name="related-topics"></a><span data-ttu-id="0bf57-206">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0bf57-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf57-207">Пошаговые инструкции по коду D3D12</span><span class="sxs-lookup"><span data-stu-id="0bf57-207">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="0bf57-208">Затенения</span><span class="sxs-lookup"><span data-stu-id="0bf57-208">Predication</span></span>](predication.md)
</dt> <dt>

[<span data-ttu-id="0bf57-209">Запросы</span><span class="sxs-lookup"><span data-stu-id="0bf57-209">Queries</span></span>](queries.md)
</dt> </dl>

 

 
