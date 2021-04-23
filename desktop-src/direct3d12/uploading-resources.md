---
title: Отправка различных типов ресурсов
description: Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103921"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="0e4c6-103">Отправка различных типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e4c6-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="0e4c6-104">Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="0e4c6-105">Использование одного буфера увеличивает гибкость использования памяти и предоставляет приложениям более строгий контроль использования памяти.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="0e4c6-106">Также показывает различия между моделями D3D11 и D3D12 для передачи различных типов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="0e4c6-107">Отправка различных типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e4c6-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="0e4c6-108">Пример кода: D3D11</span><span class="sxs-lookup"><span data-stu-id="0e4c6-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="0e4c6-109">Пример кода: D3D12</span><span class="sxs-lookup"><span data-stu-id="0e4c6-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="0e4c6-110">Константы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="0e4c6-111">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="0e4c6-112">Отражение размера ресурса</span><span class="sxs-lookup"><span data-stu-id="0e4c6-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="0e4c6-113">Выравнивание буфера</span><span class="sxs-lookup"><span data-stu-id="0e4c6-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="0e4c6-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="0e4c6-115">Отправка различных типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e4c6-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="0e4c6-116">В D3D12 приложения создают один буфер для размещения различных типов данных ресурсов для отправки и копируют данные ресурсов в один буфер аналогичным образом для различных данных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="0e4c6-117">Затем создаются отдельные представления для привязки этих данных ресурсов к графическому конвейеру в новой модели привязки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="0e4c6-118">В D3D11 приложения создают отдельные буферы для различных типов данных ресурсов (Обратите внимание на отличия, `BindFlags` которые используются в приведенном ниже примере кода D3D11), явным образом привязывает каждый буфер ресурсов к графическому конвейеру и обновляет данные ресурсов с помощью различных методов, основанных на различных типах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="0e4c6-119">Как в D3D12, так и в D3D11, приложения должны использовать только ресурсы для передачи данных, когда ЦП запишет данные один раз, и графический процессор будет считывать их один раз.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="0e4c6-120">Если GPU будет считывать данные несколько раз, GPU не будет считывать данные линейно, или визуализация в значительной степени ограничена графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="0e4c6-121">Лучшим вариантом может быть использование [**ID3D12GraphicsCommandList:: копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) или [**ID3D12GraphicsCommandList:: копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) для копирования данных буфера отправки в ресурс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="0e4c6-122">Ресурс по умолчанию может размещаться в физической видеопамяти на дискретных графических процессорах.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="0e4c6-123">Пример кода: D3D11</span><span class="sxs-lookup"><span data-stu-id="0e4c6-123">Code Example: D3D11</span></span>

``` syntax
// D3D11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-d3d12"></a><span data-ttu-id="0e4c6-124">Пример кода: D3D12</span><span class="sxs-lookup"><span data-stu-id="0e4c6-124">Code Example: D3D12</span></span>

``` syntax
// D3D12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

<span data-ttu-id="0e4c6-125">Обратите внимание на использование вспомогательных [**структур \_ CD3DX12 \_ Свойства кучи**](cd3dx12-heap-properties.md) и [**CD3DX12 \_ Resource \_ DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="0e4c6-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="0e4c6-126">Константы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-126">Constants</span></span>

<span data-ttu-id="0e4c6-127">Чтобы задать константы, вершины и индексы в куче передачи или Реадбакк, используйте следующие API:</span><span class="sxs-lookup"><span data-stu-id="0e4c6-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="0e4c6-128">**ID3D12Device:: Креатеконстантбуффервиев**</span><span class="sxs-lookup"><span data-stu-id="0e4c6-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="0e4c6-129">**ID3D12GraphicsCommandList:: Иасетвертексбуфферс**</span><span class="sxs-lookup"><span data-stu-id="0e4c6-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="0e4c6-130">**ID3D12GraphicsCommandList:: Иасетиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="0e4c6-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="0e4c6-131">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-131">Resources</span></span>

<span data-ttu-id="0e4c6-132">Ресурсы — это концепция D3D, которая абстрагирует использование физической памяти GPU.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="0e4c6-133">Ресурсы нуждаются в виртуальном адресном пространстве GPU для доступа к физической памяти.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="0e4c6-134">Создание ресурсов — это бесплатный поток.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="0e4c6-135">Существует три типа ресурсов, которые связаны с созданием виртуальных адресов и гибкостью в D3D12:</span><span class="sxs-lookup"><span data-stu-id="0e4c6-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="0e4c6-136">Зафиксированные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-136">Committed resources</span></span>

    <span data-ttu-id="0e4c6-137">Выделенные ресурсы — это наиболее распространенная идея ресурсов D3D в поколениях.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="0e4c6-138">Создание такого ресурса выделяет диапазон виртуальных адресов, неявную кучу, достаточно большую для размещения всего ресурса, и фиксирует диапазон виртуальных адресов в физической памяти, инкапсулированной в куче.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="0e4c6-139">Свойства неявной кучи должны передаваться для сопоставления функциональной четности с предыдущими версиями D3D.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="0e4c6-140">См. [**ID3D12Device:: креатекоммиттедресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="0e4c6-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="0e4c6-141">Зарезервированные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-141">Reserved resources</span></span>

    <span data-ttu-id="0e4c6-142">Зарезервированные ресурсы эквивалентны D3D11 мозаичным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="0e4c6-143">При их создании выделяется только диапазон виртуальных адресов, который не сопоставлен ни с одной кучей.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="0e4c6-144">Приложение будет сопоставлять эти ресурсы с кучами позже.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="0e4c6-145">Возможности таких ресурсов в настоящее время не изменяются по сравнению с D3D11, так как они могут быть сопоставлены с кучей с гранулярностью в 64 КБ с [**упдатетилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="0e4c6-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="0e4c6-146">См [ **. ID3D12Device:: креатересерведресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="0e4c6-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="0e4c6-147">Размещенные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-147">Placed resources</span></span>

    <span data-ttu-id="0e4c6-148">Новые для D3D12. приложения могут создавать кучи отдельно от ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="0e4c6-149">После этого приложение может располагать несколько ресурсов в одной куче.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="0e4c6-150">Это можно сделать без создания мозаичных или зарезервированных ресурсов, обеспечивая возможности для всех типов ресурсов, которые могут быть созданы непосредственно приложениями.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="0e4c6-151">Несколько ресурсов могут перекрываться, и приложение должно использовать `TiledResourceBarrier` для правильного использования физической памяти.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="0e4c6-152">См [ **. ID3D12Device:: креатеплацедресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="0e4c6-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="0e4c6-153">Отражение размера ресурса</span><span class="sxs-lookup"><span data-stu-id="0e4c6-153">Resource size reflection</span></span>

<span data-ttu-id="0e4c6-154">Приложения должны использовать отражение размера ресурса, чтобы понять, сколько текстур комнаты с неизвестными макетами текстур требуется в кучах.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="0e4c6-155">Буферы также поддерживаются, но в основном предназначены для удобства.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="0e4c6-156">Приложения должны учитывать основные несоответствия при выравнивании, чтобы обеспечить более плотную упаковку ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="0e4c6-157">Например, одноэлементный массив с однобайтовым буфером возвращает размер 64 КБ и выравнивание в 64 КБ, так как в настоящий момент буферы могут быть выровнены только 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="0e4c6-158">Кроме того, из трех массивов элементов с двумя шаг текселя 64-разрядными текстурами и с согласованным размером в один шаг текселя 4 МБ в соответствии с порядком массива задаются разные размеры.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="0e4c6-159">Если текстуры с согласованием в 4 МБ находятся в середине, то полученный размер будет 12 МБ.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="0e4c6-160">В противном случае полученный размер равен 8 МБ.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="0e4c6-161">Возвращаемое выравнивание всегда будет состоять из 4 МБ, супер набора всех выравниваний в массиве ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="0e4c6-162">Сослаться на следующие API:</span><span class="sxs-lookup"><span data-stu-id="0e4c6-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="0e4c6-163">**\_ \_ Сведения о выделении ресурсов D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="0e4c6-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="0e4c6-164">**жетресаурцеаллокатионинфо**</span><span class="sxs-lookup"><span data-stu-id="0e4c6-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="0e4c6-165">Выравнивание буфера</span><span class="sxs-lookup"><span data-stu-id="0e4c6-165">Buffer alignment</span></span>

<span data-ttu-id="0e4c6-166">Ограничения выравнивания буфера не изменяются из D3D11, особенно:</span><span class="sxs-lookup"><span data-stu-id="0e4c6-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="0e4c6-167">4 МБ для многопримерных текстур.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="0e4c6-168">64 КБ для однопримерных текстур и буферов.</span><span class="sxs-lookup"><span data-stu-id="0e4c6-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e4c6-169">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0e4c6-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e4c6-170">Подраспределение в буферах</span><span class="sxs-lookup"><span data-stu-id="0e4c6-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




