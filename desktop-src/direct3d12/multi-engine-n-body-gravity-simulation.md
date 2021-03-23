---
title: Моделирование притяжения на уровне "n-текст" для нескольких ядер
description: В примере D3D12nBodyGravity показано, как выполнять расчетные работы асинхронно.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548949"
---
# <a name="multi-engine-n-body-gravity-simulation"></a>Моделирование притяжения на уровне "n-текст" для нескольких ядер

В примере **D3D12nBodyGravity** показано, как выполнять расчетные работы асинхронно. В этом примере число потоков на каждом из них выдается с помощью очереди команд COMPUTE и планируется расчетная работа на GPU, который выполняет симуляцию притяжения в n-теле. Каждый поток работает с двумя буферами, заполненными данными о положении и скорости. При каждой итерации шейдер вычислений считывает текущие данные о положении и скорости из одного буфера и записывает следующую итерацию в другой буфер. Когда итерация завершается, шейдер вычислений меняет, какой буфер является SRV, для чтения данных о положении или скорости, а также UAV для записи обновлений расположения или скорости путем изменения состояния ресурса в каждом буфере.

-   [Создание корневых подписей](#create-the-root-signatures)
-   [Создание буферов SRV и UAV](#create-the-srv-and-uav-buffers)
-   [Создание буферов CBV и вершин](#create-the-cbv-and-vertex-buffers)
-   [Синхронизация потоков отрисовки и вычислений](#synchronize-the-rendering-and-compute-threads)
-   [Запуск примера](#run-the-sample)
-   [Связанные темы](#related-topics)

## <a name="create-the-root-signatures"></a>Создание корневых подписей

Начнем с создания графики и корневой подписи вычислений в методе **лоадассетс** . Обе корневые подписи имеют представление корневого буфера констант (CBV) и таблицу дескриптора представления ресурсов шейдера (SRV). У корневой подписи вычислений также есть таблица дескрипторов неупорядоченного представления доступа (UAV).

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| Поток вызовов                                                             | Параметры                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_Диапазон дескрипторов CD3DX12 \_**](cd3dx12-descriptor-range.md)        | [**\_Тип диапазона дескрипторов D3D12 \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**\_Корневой \_ параметр CD3DX12**](cd3dx12-root-parameter.md)            | [**\_Видимость шейдера \_ D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**\_DESC корневой \_ подписи CD3DX12 \_**](cd3dx12-root-signature-desc.md) | [**\_ \_ Флаги корневой подписи D3D12 \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_Версия корневой \_ СИГНАТУРы D3D \_**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**креатерутсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [**\_DESC корневой \_ подписи CD3DX12 \_**](cd3dx12-root-signature-desc.md) |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**\_Версия корневой \_ СИГНАТУРы D3D \_**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**креатерутсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a>Создание буферов SRV и UAV

Буферы SRV и UAV состоят из массива данных о положении и скорости.

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| Поток вызовов                       | Параметры |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a>Создание буферов CBV и вершин

Для графического конвейера CBV — это **Структура** , содержащая две матрицы, используемые шейдером Geometry. Шейдер геометрии берет на себя местоположение каждой части в системе и создает четыре, чтобы представить ее с помощью этих матриц.

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| Поток вызовов                       | Параметры |
|---------------------------------|------------|
| [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

В результате буфер вершин, используемый шейдером вершин, фактически не содержит никаких данных о позиционировании.

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| Поток вызовов                       | Параметры |
|---------------------------------|------------|
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

Для конвейера вычислений CBV — это **Структура** , содержащая некоторые константы, используемые симуляцией притяжения в виде «n-Body» в шейдере вычислений.

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a>Синхронизация потоков отрисовки и вычислений

После инициализации буферов начнется работа по отрисовке и вычислению. Поток вычислений будет изменять состояние двух буферов расположения и скорости между SRV и UAV, так как он выполняет итерацию по моделированию, а потоку отрисовки необходимо убедиться, что он работает над графическим конвейером, который работает с SRV. Границы используются для синхронизации доступа к двум буферам.

В потоке Render:

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| Поток вызовов                                                              | Параметры |
|------------------------------------------------------------------------|------------|
| [**интерлоккедексчанже**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [**интерлоккеджетвалуе**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [**жеткомплетедвалуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [**Ожидание**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

Чтобы упростить пример, поток вычислений ждет завершения каждой итерации GPU, прежде чем планировать дополнительные операции вычислений. На практике для достижения максимальной производительности GPU приложения, скорее всего, хотят, чтобы очередь вычислений была заполнена.

В потоке вычислений:

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| Поток вызовов                                                                   | Параметры |
|-----------------------------------------------------------------------------|------------|
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [**интерлоккеджетвалуе**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**Закрыть**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [**ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [**интерлоккединкремент**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [**Имел**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [**сетевентонкомплетион**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [**интерлоккеджетвалуе**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [**жеткомплетедвалуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [**Ожидание**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [**интерлоккедексчанже**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [**ID3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a>Запуск примера

![снимок экрана с окончательным моделированием "сила притяжения в тексте"](images/nbodygravity.png)

## <a name="related-topics"></a>Связанные темы

[Пошаговые инструкции по коду D3D12](d3d12-code-walk-throughs.md)

[Синхронизация с несколькими модулями](./user-mode-heap-synchronization.md)