---
title: Создание и запись списков команд и пакетов
description: В этом разделе описывается запись списков команд и пакетов в приложениях Direct3D 12. Список команд позволяет приложениям записывать вызовы рисования или изменения состояния для последующего выполнения в графическом процессоре (GPU).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480819cbd421b30cbf54a58578c02056d37d7e36bf2ead845c19e438df54cbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850719"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Создание и запись списков команд и пакетов

В этом разделе описывается запись списков команд и пакетов в приложениях Direct3D 12. Список команд позволяет приложениям записывать вызовы рисования или изменения состояния для последующего выполнения в графическом процессоре (GPU).

Помимо списков команд, функциональные возможности API используются в оборудовании GPU путем добавления второго уровня списков команд, которые называются *пакетами*. Назначение пакетов заключается в том, чтобы позволить приложениям группировать небольшое количество команд API для последующего выполнения. Во время создания пакета драйвер будет выполнять как можно более предварительную обработку, чтобы эти дешевые выполнялись позже. Пакеты предназначены для использования и повторного использования в любое количество раз. Списки команд, с другой стороны, обычно выполняются только один раз. Однако список команд *может* выполняться несколько раз (если приложение гарантирует, что предыдущие выполнения будут завершены перед отправкой новых выполнений).

Как правило, сборка вызовов API в пакеты, вызовы API и пакеты в списки команд и списки команд в одном кадре показана на следующей схеме, что означает повторное использование **пакета 1** из **списка команд 1** и **списка команд 2** и то, что имена методов API на схеме являются так же, как и примеры, можно использовать множество различных вызовов API.

![Создание команд, пакетов и списков команд в кадрах](images/gpu-workitems.png)

Существуют различные ограничения для создания и выполнения пакетов и прямых списков команд, и эти различия отмечены в этом разделе.

## <a name="creating-command-lists"></a>Создание списков команд

Списки прямых команд и пакетов создаются путем вызова [**ID3D12Device:: креатекоммандлист**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) или [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1).

Используйте [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) , чтобы создать список закрытых команд, а не создавать новый список и сразу же закрывать его. Это позволяет избежать неэффективного создания списка с распределительом и PSO, но не использует их.

[**ID3D12Device:: креатекоммандлист**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) принимает в качестве входных данных следующие параметры:

### <a name="d3d12_command_list_type"></a>\_ \_ Тип списка команд \_ D3D12

Перечисление [**\_ \_ \_ типов списка команд D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) указывает тип создаваемого списка команд. Это может быть прямой список команд, пакет, список команд для вычислений или список команд копирования.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Распределитель команд позволяет приложению управлять памятью, выделенной для списков команд. Распределитель команд создается путем вызова [**креатекоммандаллокатор**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator). При создании списка команд тип списка команд распределителя, заданный [**\_ \_ \_ типом списка команд D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type), должен соответствовать типу создаваемого списка команд. Данный распределитель может быть связан не более чем с одним в *текущий момент* списком команд одновременно, хотя для создания любого числа объектов [**графикскоммандлист**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) можно использовать один распределитель команд.

Чтобы освободить память, выделенную распределителем команд, приложение вызывает [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset). Это позволяет повторно использовать распределитель для нового команды, но не уменьшает его базовый размер. Но перед этим приложение должно убедиться, что GPU больше не выполняет все списки команд, связанные с распределителем. в противном случае вызов завершится ошибкой. Кроме того, обратите внимание, что этот API не является потокобезопасным и, следовательно, не может быть вызван в одном распределителе одновременно из нескольких потоков.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

Начальное состояние конвейера для списка команд. В Microsoft Direct3D 12 большинство состояний графического конвейера задаются в списке команд с помощью объекта [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) . Приложение создает большое количество таких объектов, как правило, во время инициализации приложения, а затем обновляет состояние, изменяя текущее привязанное состояние с помощью [**ID3D12GraphicsCommandList:: сетпипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate). Дополнительные сведения об объектах состояния конвейера см. [в разделе Управление состоянием графического конвейера в Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

Обратите внимание, что пакеты не наследуют состояние конвейера, установленное предыдущими вызовами в списках прямых команд, являющихся родительскими.

Если этот параметр имеет значение NULL, используется состояние по умолчанию.

## <a name="recording-command-lists"></a>Запись списков команд

Сразу после создания списки команд находятся в состоянии записи. Можно также повторно использовать существующий список команд, вызвав I [**D3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset), который также оставляет список команд в состоянии записи. В отличие от [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset), можно вызвать **Reset** , пока список команд еще выполняется. Типичный шаблон — отправить список команд и сразу же сбросить его, чтобы повторно использовать выделенную память для другого списка команд. Обратите внимание, что один список команд, связанный с каждым распределителем команд, может находиться в состоянии записи одновременно.

Когда список команд находится в состоянии записи, просто вызывайте методы интерфейса [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , чтобы добавить команды в список. Многие из этих методов позволяют реализовать общие функции Direct3D, которые будут знакомы разработчикам Microsoft Direct3D 11; другие интерфейсы API являются новыми для Direct3D 12.

После добавления команд в список команд можно перевести список команд из состояния записи, вызвав [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).

Распределитель команд может увеличиваться, но не сжимать пулы и повторно использовать распределительы, чтобы максимально повысить эффективность работы приложения. Можно записать несколько списков в один распределитель, прежде чем он будет сброшен, при условии, что только один список записывается в данный распределитель одновременно. Можно визуализировать каждый список как владеющий частью распределителя, который указывает, что будет выполняться [**ID3D12CommandQueue:: ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) .

Простая стратегия пула распределителя должна быть ориентирована на примерно `numCommandLists * MaxFrameLatency` распределительы. Например, если вы записываете 6 списков и допускаете до 3 скрытых кадров, вы можете рассчитывать на 18-20 распределителя. Более сложная стратегия объединения в пул, которая повторно использует распределителя для нескольких списков в одном потоке, может быть предпринята для `numRecordingThreads * MaxFrameLatency` распределительов. В предыдущем примере, если два списка были записаны в поток а, 2 в потоке B, 1 в потоке C и 1 в потоке D, можно было бы реалистично приступать к 12-14 распределителя.

Используйте ограждение, чтобы определить, когда можно повторно использовать данный распределитель.

Так как списки команд можно сразу же сбросить после выполнения, они могут быть тривиальны в пул, добавляя их обратно в пул после каждого вызова [**ID3D12CommandQueue:: ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="example"></a>Пример

В следующих фрагментах кода показано создание и запись списка команд. Обратите внимание, что этот пример включает следующие функции Direct3D 12:

-   Объекты состояния конвейера — используются для установки большинства параметров состояния конвейера отрисовки из списка команд. Дополнительные сведения см. [в разделе Управление состоянием графического конвейера в Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).
-   Куча дескрипторов. приложения используют кучи дескрипторов для управления привязкой конвейера к ресурсам памяти.
-   Барьер ресурсов — используется для управления переходом ресурсов из одного состояния в другое, например из представления целевого объекта прорисовки в представление ресурсов шейдера. Дополнительные сведения см. [в статье использование барьеров ресурсов для синхронизации состояний ресурсов](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

Например,


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



После создания и записи списка команд его можно выполнить с помощью очереди команд. Дополнительные сведения см. в разделе [исполнение и синхронизация списков команд](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Подсчет ссылок

Большинство API D3D12 по-прежнему используют подсчет ссылок в соответствии с соглашениями COM. Важным исключением является интерфейс API списка команд D3D12 Graphics. Все API-интерфейсы в [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) не содержат ссылок на объекты, передаваемые в эти API. Это означает, что приложения несут ответственность за то, чтобы список команд никогда не отправлялся для выполнения, который ссылается на уничтоженный ресурс.

## <a name="command-list-errors"></a>Ошибки списка команд

Большинство API-интерфейсов в [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) не возвращают ошибки. Ошибки, обнаруженные при создании списка команд, откладываются до [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close). Единственным исключением является \_ \_ Удаление устройства с ошибкой DXGI \_ , которое откладывается еще дальше. Обратите внимание, что это отличается от D3D11, где многие ошибки проверки параметров автоматически удаляются и никогда не возвращаются вызывающему.

Приложения могут видеть \_ ошибки удаленных устройств DXGI \_ в следующих вызовах API:

-   Любой метод создания ресурсов
-   [**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Ограничения API списка команд

Некоторые API-интерфейсы списка команд могут вызываться только для определенных типов списков команд. В таблице ниже показано, какие интерфейсы API списка команд допустимы для вызова для каждого типа списка команд. Он также показывает, какие интерфейсы API являются допустимыми для вызова в [**ходе D3D12 подготовки к просмотру**](./direct3d-12-render-passes.md). 

| Имя API                                         | Графика | Вычисления | Копировать | Bundle | В ходе подготовки к просмотру |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginQuery                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Ограничения пакета

Ограничения позволяют драйверам Direct3D 12 выполнять большую часть работы, связанную с пакетами во время записи, тем самым позволяя запускать API [**ексекутебундле**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) с низкими издержками. Все объекты состояния конвейера, на которые ссылается пакет, должны иметь одинаковые форматы целевого объекта рендеринга, формат буфера глубины и примеры описаний.

Следующие команды API не допускаются для списков команд, созданных с помощью типа: D3D12 \_ \_ \_ набор типов списка команд \_ :

-   Любой метод Clear
-   Любой метод Copy
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

[**Сетдескрипторхеапс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) можно вызывать для пакета, но кучи дескрипторов наборов должны соответствовать куче дескрипторов списка команд.

Если какой-либо из этих интерфейсов API вызывается в пакете, среда выполнения удаляет вызов. При возникновении этой ошибки отладочный слой выдаст ошибку.

## <a name="related-topics"></a>Связанные темы

[Отправка работы в Direct3D 12](command-queues-and-command-lists.md)