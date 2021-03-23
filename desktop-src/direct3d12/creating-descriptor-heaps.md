---
title: Создание куч дескрипторов
description: Чтобы создать и настроить кучу дескрипторов, необходимо выбрать тип кучи дескрипторов, определить количество содержащихся в нем дескрипторов и установить флаги, указывающие, является ли он видимым и/или видимым для шейдера.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e472a0749634d5cbaa9cbf1cde5e11202d4c4f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548945"
---
# <a name="creating-descriptor-heaps"></a><span data-ttu-id="32274-103">Создание куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-103">Creating Descriptor Heaps</span></span>

<span data-ttu-id="32274-104">Чтобы создать и настроить кучу дескрипторов, необходимо выбрать тип кучи дескрипторов, определить количество содержащихся в нем дескрипторов и установить флаги, указывающие, является ли он видимым и/или видимым для шейдера.</span><span class="sxs-lookup"><span data-stu-id="32274-104">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span>

-   [<span data-ttu-id="32274-105">Типы кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-105">Descriptor Heap types</span></span>](#descriptor-heap-types)
-   [<span data-ttu-id="32274-106">Свойства кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-106">Descriptor Heap Properties</span></span>](#descriptor-heap-properties)
-   [<span data-ttu-id="32274-107">Указатели дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-107">Descriptor Handles</span></span>](#descriptor-handles)
-   [<span data-ttu-id="32274-108">Методы кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-108">Descriptor Heap Methods</span></span>](#descriptor-heap-methods)
-   [<span data-ttu-id="32274-109">Оболочка минимального дескриптора кучи</span><span class="sxs-lookup"><span data-stu-id="32274-109">Minimal descriptor heap wrapper</span></span>](#minimal-descriptor-heap-wrapper)
-   [<span data-ttu-id="32274-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="32274-110">Related topics</span></span>](#related-topics)

## <a name="descriptor-heap-types"></a><span data-ttu-id="32274-111">Типы кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-111">Descriptor Heap types</span></span>

<span data-ttu-id="32274-112">Тип кучи определяется одним элементом перечисления [**\_ \_ \_ типа кучи дескриптора D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :</span><span class="sxs-lookup"><span data-stu-id="32274-112">The type of heap is determined by one member of the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) enum:</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a><span data-ttu-id="32274-113">Свойства кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-113">Descriptor Heap Properties</span></span>

<span data-ttu-id="32274-114">Свойства кучи задаются в [**структуре \_ \_ \_ DESC дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , которая ссылается на перечисление [**\_ \_ \_ типов кучи дескрипторов D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) и [**D3D12 с \_ \_ \_ флагами кучи дескриптора**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) .</span><span class="sxs-lookup"><span data-stu-id="32274-114">Heap properties are set on the [**D3D12\_DESCRIPTOR\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) structure, which references both the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) and [**D3D12\_DESCRIPTOR\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) enums.</span></span>

<span data-ttu-id="32274-115">Флажок флага \_ кучи дескрипторов D3D12 \_ \_ \_ \_ можно установить в куче дескрипторов, чтобы указать, что он привязан к списку команд для ссылки с помощью шейдеров.</span><span class="sxs-lookup"><span data-stu-id="32274-115">The flag D3D12\_DESCRIPTOR\_HEAP\_FLAG\_SHADER\_VISIBLE can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders.</span></span> <span data-ttu-id="32274-116">Кучи дескрипторов, созданные *без* этого флага, позволяют приложениям создавать дескрипторы в памяти ЦП перед их копированием в видимую кучу дескрипторов шейдера для удобства.</span><span class="sxs-lookup"><span data-stu-id="32274-116">Descriptor heaps created *without* this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience.</span></span> <span data-ttu-id="32274-117">Но в приложениях также есть возможность непосредственно создавать дескрипторы в кучах дескрипторов, видимых шейдеру, без необходимости размещения чего-либо на ЦП.</span><span class="sxs-lookup"><span data-stu-id="32274-117">But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.</span></span>

<span data-ttu-id="32274-118">Этот флаг применяется только к CBV, SRV, UAV и пробам.</span><span class="sxs-lookup"><span data-stu-id="32274-118">This flag only applies to CBV, SRV, UAV and samplers.</span></span> <span data-ttu-id="32274-119">Он не применяется к другим типам кучи дескрипторов, поскольку шейдеры не ссылаются напрямую на другие типы.</span><span class="sxs-lookup"><span data-stu-id="32274-119">It does not apply to other descriptor heap types since shaders do not directly reference the other types.</span></span>

<span data-ttu-id="32274-120">Например, опишите и создайте кучу дескрипторов образцов.</span><span class="sxs-lookup"><span data-stu-id="32274-120">For example, describe and create a sampler descriptor heap.</span></span>


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



<span data-ttu-id="32274-121">Опишите и создайте представление буфера констант (CBV), представление ресурсов шейдера (SRV) и кучу дескрипторов неупорядоченного представления доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="32274-121">Describe and create a constant buffer view (CBV), Shader resource view (SRV), and unordered access view (UAV) descriptor heap.</span></span>


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a><span data-ttu-id="32274-122">Указатели дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-122">Descriptor Handles</span></span>

<span data-ttu-id="32274-123">Структуры дескрипторов [**\_ GPU D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) и [**\_ \_ \_ обработчики дескрипторов ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) обозначают определенные дескрипторы в куче дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="32274-123">The [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) and [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structures identify specific descriptors in a descriptor heap.</span></span> <span data-ttu-id="32274-124">Маркер является немного похожим на указатель, но приложение не должно вручную отменять ссылку на него; в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="32274-124">A handle is a bit like a pointer, but the application must not dereference it manually; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="32274-125">Использование дескрипторов должно проходить через API.</span><span class="sxs-lookup"><span data-stu-id="32274-125">The use of the handles must go through the API.</span></span> <span data-ttu-id="32274-126">Сам дескриптор может быть свободно скопирован или передан в интерфейсы API, которые работают с дескрипторами и используют их.</span><span class="sxs-lookup"><span data-stu-id="32274-126">A handle itself can be copied freely or passed into APIs that operate on/use descriptors.</span></span> <span data-ttu-id="32274-127">Нет подсчета ссылок, поэтому приложение должно убедиться, что оно не использует дескриптор после удаления базовой кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="32274-127">There is no ref counting, so the application must ensure that it does not use a handle after the underlying descriptor heap has been deleted.</span></span>

<span data-ttu-id="32274-128">Приложения могут определить размер приращения дескрипторов для заданного типа кучи дескрипторов, чтобы они могли создавать дескрипторы любого расположения в куче дескрипторов вручную, начиная от дескриптора до базового класса.</span><span class="sxs-lookup"><span data-stu-id="32274-128">Applications can find out the increment size of the descriptors for a given descriptor heap type, so that they can generate handles to any location in a descriptor heap manually starting from the handle to the base.</span></span> <span data-ttu-id="32274-129">Приложения не должны жестко закодировать размер дескриптора, и всегда должны запрашивать их для конкретного экземпляра устройства; в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="32274-129">Applications must never hardcode descriptor handle increment sizes, and should always query them for a given device instance; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="32274-130">Приложения также не должны использовать размеры и дескрипторы приращения для выполнения собственных операций проверки или обработки данных в куче дескрипторов, так как результаты этого не определены.</span><span class="sxs-lookup"><span data-stu-id="32274-130">Applications must also not use the increment sizes and handles to do their own examination or manipulation of descriptor heap data, as the results from doing so are undefined.</span></span> <span data-ttu-id="32274-131">Дескрипторы могут фактически не использоваться как указатели, а как прокси для указателей, чтобы избежать случайного разыменования.</span><span class="sxs-lookup"><span data-stu-id="32274-131">The handles may not actually be used as pointers, but rather as proxies for pointers so as to avoid accidental dereferencing.</span></span>

> [!Note]
>
> <span data-ttu-id="32274-132">Существует вспомогательная структура, \_ дескриптор GPU CD3DX12 \_ \_ , определенный в заголовке d3dx12. h, который наследует структуру [**\_ \_ \_ дескрипторов GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) и обеспечивает инициализацию и другие полезные операции.</span><span class="sxs-lookup"><span data-stu-id="32274-132">There is a helper structure, CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, defined in the header d3dx12.h, which inherits the [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure and provides initialization and other useful operations.</span></span> <span data-ttu-id="32274-133">Аналогично \_ вспомогательная структура дескриптора ЦП CD3DX12 \_ \_ определяется для структуры [**\_ \_ \_ дескриптора процессора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="32274-133">Similarly the CD3DX12\_CPU\_DESCRIPTOR\_HANDLE helper structure is defined for the [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

 

<span data-ttu-id="32274-134">Обе эти вспомогательные структуры используются при заполнении списков команд.</span><span class="sxs-lookup"><span data-stu-id="32274-134">Both of these helper structures are used when populating command lists.</span></span>


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a><span data-ttu-id="32274-135">Методы кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-135">Descriptor Heap Methods</span></span>

<span data-ttu-id="32274-136">Кучи дескрипторов ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) наследуют от [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span><span class="sxs-lookup"><span data-stu-id="32274-136">Descriptor heaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) inherit from [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span></span> <span data-ttu-id="32274-137">Это налагает ответственность за местонахождение управления кучами дескрипторов в приложениях, так же, как кучи ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32274-137">This imposes the responsibility for the residency management of descriptor heaps on applications, just like resource heaps.</span></span> <span data-ttu-id="32274-138">Методы управления местонахождение применяются только к видимым кучам шейдера, так как невидимые кучи без шейдера не видны непосредственно GPU.</span><span class="sxs-lookup"><span data-stu-id="32274-138">The residency management methods only apply to shader visible heaps since the non shader visible heaps are not visible to the GPU directly.</span></span>

<span data-ttu-id="32274-139">Метод [**ID3D12Device:: жетдескрипторхандлеинкрементсизе**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) позволяет приложениям вручную смещать дескрипторы в кучу (создавая дескрипторы в любом месте кучи дескрипторов).</span><span class="sxs-lookup"><span data-stu-id="32274-139">The [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) method allows applications to manually offset handles into a heap (producing handles into anywhere in a descriptor heap).</span></span> <span data-ttu-id="32274-140">Маркер начального расположения кучи поступает из [**ID3D12DescriptorHeap:: жеткпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: жетгпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span><span class="sxs-lookup"><span data-stu-id="32274-140">The heap start location’s handle comes from [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)/[**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span></span> <span data-ttu-id="32274-141">Смещение выполняется путем добавления размера приращения количества дескрипторов, \* которые должны быть смещены на начало кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="32274-141">Offsetting is done by adding the increment size \* the number of descriptors to offset to the descriptor heap start .</span></span> <span data-ttu-id="32274-142">Обратите внимание, что размер приращения не может рассматриваться как размер в байтах, так как приложения не должны обращаться к дескрипторам, как если бы они были памятью — память, на которую указывает нестандартизированный макет, может различаться даже для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="32274-142">Note that the increment size cannot be thought of as a byte size since applications must not dereference handles as if they are memory – the memory pointed to has a non-standardized layout and can vary even for a given device.</span></span>

<span data-ttu-id="32274-143">[**Жеткпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) ВОЗВРАЩАЕТ дескриптор ЦП для куч видимого дескриптора ЦП.</span><span class="sxs-lookup"><span data-stu-id="32274-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) returns a CPU handle for CPU visible descriptor heaps.</span></span> <span data-ttu-id="32274-144">Он возвращает дескриптор NULL (и отладочный слой сообщит об ошибке), если куча дескриптора не является видимой для ЦП.</span><span class="sxs-lookup"><span data-stu-id="32274-144">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not CPU visible.</span></span>

<span data-ttu-id="32274-145">[**Жетгпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) ВОЗВРАЩАЕТ дескриптор GPU для куч видимых дескрипторов шейдеров.</span><span class="sxs-lookup"><span data-stu-id="32274-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) returns a GPU handle for shader visible descriptor heaps.</span></span> <span data-ttu-id="32274-146">Он возвращает дескриптор NULL (и отладочный слой сообщит об ошибке), если куча дескриптора не видна шейдеру.</span><span class="sxs-lookup"><span data-stu-id="32274-146">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not shader visible.</span></span>

<span data-ttu-id="32274-147">Например, создание представлений целевого объекта рендеринга для отображения текста D2D с помощью устройства 11on12.</span><span class="sxs-lookup"><span data-stu-id="32274-147">For example, creating render target views to display D2D text using an 11on12 device.</span></span>


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a><span data-ttu-id="32274-148">Оболочка минимального дескриптора кучи</span><span class="sxs-lookup"><span data-stu-id="32274-148">Minimal descriptor heap wrapper</span></span>

<span data-ttu-id="32274-149">Разработчикам приложений, скорее всего, потребуется создать собственный вспомогательный код для управления дескрипторами дескрипторов и кучами.</span><span class="sxs-lookup"><span data-stu-id="32274-149">Application developers will likely want to build their own helper code for managing descriptor handles and heaps.</span></span> <span data-ttu-id="32274-150">Ниже приведен простой пример.</span><span class="sxs-lookup"><span data-stu-id="32274-150">A basic example is shown below.</span></span> <span data-ttu-id="32274-151">Более сложные оболочки могут, например, отследить, какие типы дескрипторов находятся в куче и хранят аргументы создания дескриптора.</span><span class="sxs-lookup"><span data-stu-id="32274-151">More sophisticated wrappers could, for example, keep track of what types of descriptors are where in a heap and store the descriptor creation arguments.</span></span>

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a><span data-ttu-id="32274-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="32274-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32274-153">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="32274-153">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 