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
# <a name="creating-descriptor-heaps"></a>Создание куч дескрипторов

Чтобы создать и настроить кучу дескрипторов, необходимо выбрать тип кучи дескрипторов, определить количество содержащихся в нем дескрипторов и установить флаги, указывающие, является ли он видимым и/или видимым для шейдера.

-   [Типы кучи дескрипторов](#descriptor-heap-types)
-   [Свойства кучи дескрипторов](#descriptor-heap-properties)
-   [Указатели дескрипторов](#descriptor-handles)
-   [Методы кучи дескрипторов](#descriptor-heap-methods)
-   [Оболочка минимального дескриптора кучи](#minimal-descriptor-heap-wrapper)
-   [Связанные темы](#related-topics)

## <a name="descriptor-heap-types"></a>Типы кучи дескрипторов

Тип кучи определяется одним элементом перечисления [**\_ \_ \_ типа кучи дескриптора D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :

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

## <a name="descriptor-heap-properties"></a>Свойства кучи дескрипторов

Свойства кучи задаются в [**структуре \_ \_ \_ DESC дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , которая ссылается на перечисление [**\_ \_ \_ типов кучи дескрипторов D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) и [**D3D12 с \_ \_ \_ флагами кучи дескриптора**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) .

Флажок флага \_ кучи дескрипторов D3D12 \_ \_ \_ \_ можно установить в куче дескрипторов, чтобы указать, что он привязан к списку команд для ссылки с помощью шейдеров. Кучи дескрипторов, созданные *без* этого флага, позволяют приложениям создавать дескрипторы в памяти ЦП перед их копированием в видимую кучу дескрипторов шейдера для удобства. Но в приложениях также есть возможность непосредственно создавать дескрипторы в кучах дескрипторов, видимых шейдеру, без необходимости размещения чего-либо на ЦП.

Этот флаг применяется только к CBV, SRV, UAV и пробам. Он не применяется к другим типам кучи дескрипторов, поскольку шейдеры не ссылаются напрямую на другие типы.

Например, опишите и создайте кучу дескрипторов образцов.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Опишите и создайте представление буфера констант (CBV), представление ресурсов шейдера (SRV) и кучу дескрипторов неупорядоченного представления доступа (UAV).


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



## <a name="descriptor-handles"></a>Указатели дескрипторов

Структуры дескрипторов [**\_ GPU D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) и [**\_ \_ \_ обработчики дескрипторов ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) обозначают определенные дескрипторы в куче дескрипторов. Маркер является немного похожим на указатель, но приложение не должно вручную отменять ссылку на него; в противном случае поведение не определено. Использование дескрипторов должно проходить через API. Сам дескриптор может быть свободно скопирован или передан в интерфейсы API, которые работают с дескрипторами и используют их. Нет подсчета ссылок, поэтому приложение должно убедиться, что оно не использует дескриптор после удаления базовой кучи дескрипторов.

Приложения могут определить размер приращения дескрипторов для заданного типа кучи дескрипторов, чтобы они могли создавать дескрипторы любого расположения в куче дескрипторов вручную, начиная от дескриптора до базового класса. Приложения не должны жестко закодировать размер дескриптора, и всегда должны запрашивать их для конкретного экземпляра устройства; в противном случае поведение не определено. Приложения также не должны использовать размеры и дескрипторы приращения для выполнения собственных операций проверки или обработки данных в куче дескрипторов, так как результаты этого не определены. Дескрипторы могут фактически не использоваться как указатели, а как прокси для указателей, чтобы избежать случайного разыменования.

> [!Note]
>
> Существует вспомогательная структура, \_ дескриптор GPU CD3DX12 \_ \_ , определенный в заголовке d3dx12. h, который наследует структуру [**\_ \_ \_ дескрипторов GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) и обеспечивает инициализацию и другие полезные операции. Аналогично \_ вспомогательная структура дескриптора ЦП CD3DX12 \_ \_ определяется для структуры [**\_ \_ \_ дескриптора процессора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

 

Обе эти вспомогательные структуры используются при заполнении списков команд.


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



## <a name="descriptor-heap-methods"></a>Методы кучи дескрипторов

Кучи дескрипторов ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) наследуют от [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Это налагает ответственность за местонахождение управления кучами дескрипторов в приложениях, так же, как кучи ресурсов. Методы управления местонахождение применяются только к видимым кучам шейдера, так как невидимые кучи без шейдера не видны непосредственно GPU.

Метод [**ID3D12Device:: жетдескрипторхандлеинкрементсизе**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) позволяет приложениям вручную смещать дескрипторы в кучу (создавая дескрипторы в любом месте кучи дескрипторов). Маркер начального расположения кучи поступает из [**ID3D12DescriptorHeap:: жеткпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: жетгпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). Смещение выполняется путем добавления размера приращения количества дескрипторов, \* которые должны быть смещены на начало кучи дескрипторов. Обратите внимание, что размер приращения не может рассматриваться как размер в байтах, так как приложения не должны обращаться к дескрипторам, как если бы они были памятью — память, на которую указывает нестандартизированный макет, может различаться даже для конкретного устройства.

[**Жеткпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) ВОЗВРАЩАЕТ дескриптор ЦП для куч видимого дескриптора ЦП. Он возвращает дескриптор NULL (и отладочный слой сообщит об ошибке), если куча дескриптора не является видимой для ЦП.

[**Жетгпудескрипторхандлефорхеапстарт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) ВОЗВРАЩАЕТ дескриптор GPU для куч видимых дескрипторов шейдеров. Он возвращает дескриптор NULL (и отладочный слой сообщит об ошибке), если куча дескриптора не видна шейдеру.

Например, создание представлений целевого объекта рендеринга для отображения текста D2D с помощью устройства 11on12.


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



## <a name="minimal-descriptor-heap-wrapper"></a>Оболочка минимального дескриптора кучи

Разработчикам приложений, скорее всего, потребуется создать собственный вспомогательный код для управления дескрипторами дескрипторов и кучами. Ниже приведен простой пример. Более сложные оболочки могут, например, отследить, какие типы дескрипторов находятся в куче и хранят аргументы создания дескриптора.

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Кучи дескрипторов](descriptor-heaps.md)
</dt> </dl>

 

 