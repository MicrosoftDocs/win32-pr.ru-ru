---
title: Отправка различных типов ресурсов
description: Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563784"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="89589-103">Отправка различных типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="89589-103">Uploading different types of resources</span></span>

<span data-ttu-id="89589-104">Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах.</span><span class="sxs-lookup"><span data-stu-id="89589-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="89589-105">Использование одного буфера увеличивает гибкость использования памяти и предоставляет приложения с более жестким контролем за использованием памяти.</span><span class="sxs-lookup"><span data-stu-id="89589-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="89589-106">Также показывает различия между моделями Direct3D 11 и Direct3D 12 для передачи различных типов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89589-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="89589-107">Upload различных типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="89589-107">Upload different types of resources</span></span>

<span data-ttu-id="89589-108">В Direct3D 12 вы создаете один буфер для размещения различных типов данных ресурсов для отправки, а данные ресурсов копируются в один буфер аналогичным образом для различных данных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89589-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="89589-109">Затем создаются отдельные представления для привязки этих данных ресурсов к графическому конвейеру в модели привязки ресурсов Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="89589-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="89589-110">В Direct3D 11 вы создаете отдельные буферы для различных типов данных ресурсов (Обратите внимание на различные `BindFlags` примеры, используемые в приведенном ниже примере Direct3D 11), явно привязывает каждый буфер ресурсов к графическому конвейеру и обновляете данные ресурсов с помощью различных методов, основанных на различных типах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89589-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="89589-111">В Direct3D 12 и Direct3D 11 следует использовать загрузку ресурсов только в том случае, когда ЦП запишет данные один раз, и GPU прочитает их один раз.</span><span class="sxs-lookup"><span data-stu-id="89589-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="89589-112">В некоторых случаях</span><span class="sxs-lookup"><span data-stu-id="89589-112">In some cases,</span></span>
* <span data-ttu-id="89589-113">GPU будет считывать данные несколько раз, или</span><span class="sxs-lookup"><span data-stu-id="89589-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="89589-114">GPU не считывает данные линейно или</span><span class="sxs-lookup"><span data-stu-id="89589-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="89589-115">отрисовка в значительной степени ограничена GPU.</span><span class="sxs-lookup"><span data-stu-id="89589-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="89589-116">В таких случаях лучшим вариантом может быть использование [**ID3D12GraphicsCommandList:: копитекстуререгион**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) или [**ID3D12GraphicsCommandList:: копибуфферрегион**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) для копирования данных буфера отправки в ресурс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89589-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="89589-117">Ресурс по умолчанию может размещаться в физической видеопамяти на дискретных графических процессорах.</span><span class="sxs-lookup"><span data-stu-id="89589-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="89589-118">Пример кода: Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="89589-118">Code Example: Direct3D 11</span></span>

```cpp
// Direct3D 11: Separate buffers for each resource type.

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

### <a name="code-example-direct3d-12"></a><span data-ttu-id="89589-119">Пример кода: Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="89589-119">Code Example: Direct3D 12</span></span>

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

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

<span data-ttu-id="89589-120">Обратите внимание на использование вспомогательных структур [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) и [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="89589-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="89589-121">Константы</span><span class="sxs-lookup"><span data-stu-id="89589-121">Constants</span></span>

<span data-ttu-id="89589-122">Чтобы задать константы, вершины и индексы в куче передачи или реадбакк, используйте следующие API.</span><span class="sxs-lookup"><span data-stu-id="89589-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="89589-123">**ID3D12Device:: Креатеконстантбуффервиев**</span><span class="sxs-lookup"><span data-stu-id="89589-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="89589-124">**ID3D12GraphicsCommandList:: Иасетвертексбуфферс**</span><span class="sxs-lookup"><span data-stu-id="89589-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="89589-125">**ID3D12GraphicsCommandList:: Иасетиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="89589-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="89589-126">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="89589-126">Resources</span></span>

<span data-ttu-id="89589-127">Ресурсы — это концепция Direct3D, которая абстрагирует использование физической памяти GPU.</span><span class="sxs-lookup"><span data-stu-id="89589-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="89589-128">Ресурсы нуждаются в виртуальном адресном пространстве GPU для доступа к физической памяти.</span><span class="sxs-lookup"><span data-stu-id="89589-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="89589-129">Создание ресурсов — это бесплатный поток.</span><span class="sxs-lookup"><span data-stu-id="89589-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="89589-130">Существует три типа ресурсов, которые связаны с созданием виртуальных адресов и гибкостью в Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="89589-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="89589-131">Зафиксированные ресурсы</span><span class="sxs-lookup"><span data-stu-id="89589-131">Committed resources</span></span>

<span data-ttu-id="89589-132">Выделенные ресурсы являются наиболее распространенной концепцией ресурсов Direct3D в поколении.</span><span class="sxs-lookup"><span data-stu-id="89589-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="89589-133">Создание такого ресурса выделяет диапазон виртуальных адресов, неявную кучу, достаточно большую для размещения всего ресурса, и фиксирует диапазон виртуальных адресов в физической памяти, инкапсулированной в куче.</span><span class="sxs-lookup"><span data-stu-id="89589-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="89589-134">Свойства неявной кучи должны передаваться для сопоставления функциональной четности с предыдущими версиями Direct3D.</span><span class="sxs-lookup"><span data-stu-id="89589-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="89589-135">См. [**ID3D12Device:: креатекоммиттедресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="89589-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="89589-136">Зарезервированные ресурсы</span><span class="sxs-lookup"><span data-stu-id="89589-136">Reserved resources</span></span>

<span data-ttu-id="89589-137">Зарезервированные ресурсы эквивалентны мозаичным ресурсам Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="89589-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="89589-138">При их создании выделяется только диапазон виртуальных адресов, который не сопоставляется ни с одной кучей.</span><span class="sxs-lookup"><span data-stu-id="89589-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="89589-139">Приложение будет сопоставлять эти ресурсы с кучами позже.</span><span class="sxs-lookup"><span data-stu-id="89589-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="89589-140">Возможности таких ресурсов в настоящее время не изменяются с Direct3D 11, так как они могут быть сопоставлены с кучей на уровне гранулярности в 64 КБ с [**упдатетилемаппингс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="89589-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="89589-141">См. [**ID3D12Device:: креатересерведресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span><span class="sxs-lookup"><span data-stu-id="89589-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="89589-142">Размещенные ресурсы</span><span class="sxs-lookup"><span data-stu-id="89589-142">Placed resources</span></span>

<span data-ttu-id="89589-143">Новая возможность для Direct3D 12 позволяет создавать кучи отдельно от ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89589-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="89589-144">После этого можно будет выбрать несколько ресурсов в одной куче.</span><span class="sxs-lookup"><span data-stu-id="89589-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="89589-145">Это можно сделать без создания мозаичных или зарезервированных ресурсов, обеспечивая возможности для всех типов ресурсов, которые могут быть созданы непосредственно приложением.</span><span class="sxs-lookup"><span data-stu-id="89589-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="89589-146">Несколько ресурсов могут перекрываться, и необходимо использовать [**ID3D12GraphicsCommandList:: ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) для правильной повторного использования физической памяти.</span><span class="sxs-lookup"><span data-stu-id="89589-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="89589-147">См. [**ID3D12Device:: креатеплацедресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span><span class="sxs-lookup"><span data-stu-id="89589-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="89589-148">Отражение размера ресурса</span><span class="sxs-lookup"><span data-stu-id="89589-148">Resource size reflection</span></span>

<span data-ttu-id="89589-149">Используйте отражение размера ресурса, чтобы понять, сколько текстур пространства с неизвестными макетами текстур требуется в кучах.</span><span class="sxs-lookup"><span data-stu-id="89589-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="89589-150">Буферы также поддерживаются, но в основном предназначены для удобства.</span><span class="sxs-lookup"><span data-stu-id="89589-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="89589-151">Вы должны знать о несоответствиях основного выравнивания, чтобы обеспечить более плотную упаковку ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89589-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="89589-152">Например, одноэлементный массив с однобайтовым буфером возвращает *Размер* 64 КБ и *Выравнивание* в 64 КБ, поскольку буферы могут быть только 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="89589-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="89589-153">Кроме того, из трех массивов элементов с двумя шаг текселя 64-разрядными текстурами и с согласованным размером в один шаг текселя 4 МБ в соответствии с порядком массива задаются разные размеры.</span><span class="sxs-lookup"><span data-stu-id="89589-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="89589-154">Если текстуры с согласованием в 4 МБ находятся в середине, то полученный *Размер* будет 12 МБ.</span><span class="sxs-lookup"><span data-stu-id="89589-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="89589-155">В противном случае полученный размер равен 8 МБ.</span><span class="sxs-lookup"><span data-stu-id="89589-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="89589-156">Возвращаемое выравнивание всегда будет равно 4 МБ, супермножество всех выравниваний в массиве ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89589-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="89589-157">Сослаться на следующие API.</span><span class="sxs-lookup"><span data-stu-id="89589-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="89589-158">**\_ \_ Сведения о выделении ресурсов D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="89589-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="89589-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="89589-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="89589-160">Выравнивание буфера</span><span class="sxs-lookup"><span data-stu-id="89589-160">Buffer alignment</span></span>

<span data-ttu-id="89589-161">Ограничения выравнивания буфера не изменялись с Direct3D 11, особенно:</span><span class="sxs-lookup"><span data-stu-id="89589-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="89589-162">4 МБ для многопримерных текстур.</span><span class="sxs-lookup"><span data-stu-id="89589-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="89589-163">64 КБ для однопримерных текстур и буферов.</span><span class="sxs-lookup"><span data-stu-id="89589-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89589-164">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="89589-164">Related topics</span></span>

* [<span data-ttu-id="89589-165">Подраспределение в буферах</span><span class="sxs-lookup"><span data-stu-id="89589-165">Suballocation within buffers</span></span>](large-buffers.md)
