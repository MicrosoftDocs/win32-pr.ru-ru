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
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="66eac-103">Моделирование притяжения на уровне "n-текст" для нескольких ядер</span><span class="sxs-lookup"><span data-stu-id="66eac-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="66eac-104">В примере **D3D12nBodyGravity** показано, как выполнять расчетные работы асинхронно.</span><span class="sxs-lookup"><span data-stu-id="66eac-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="66eac-105">В этом примере число потоков на каждом из них выдается с помощью очереди команд COMPUTE и планируется расчетная работа на GPU, который выполняет симуляцию притяжения в n-теле.</span><span class="sxs-lookup"><span data-stu-id="66eac-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="66eac-106">Каждый поток работает с двумя буферами, заполненными данными о положении и скорости.</span><span class="sxs-lookup"><span data-stu-id="66eac-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="66eac-107">При каждой итерации шейдер вычислений считывает текущие данные о положении и скорости из одного буфера и записывает следующую итерацию в другой буфер.</span><span class="sxs-lookup"><span data-stu-id="66eac-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="66eac-108">Когда итерация завершается, шейдер вычислений меняет, какой буфер является SRV, для чтения данных о положении или скорости, а также UAV для записи обновлений расположения или скорости путем изменения состояния ресурса в каждом буфере.</span><span class="sxs-lookup"><span data-stu-id="66eac-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="66eac-109">Создание корневых подписей</span><span class="sxs-lookup"><span data-stu-id="66eac-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="66eac-110">Создание буферов SRV и UAV</span><span class="sxs-lookup"><span data-stu-id="66eac-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="66eac-111">Создание буферов CBV и вершин</span><span class="sxs-lookup"><span data-stu-id="66eac-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="66eac-112">Синхронизация потоков отрисовки и вычислений</span><span class="sxs-lookup"><span data-stu-id="66eac-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="66eac-113">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="66eac-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="66eac-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="66eac-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="66eac-115">Создание корневых подписей</span><span class="sxs-lookup"><span data-stu-id="66eac-115">Create the root signatures</span></span>

<span data-ttu-id="66eac-116">Начнем с создания графики и корневой подписи вычислений в методе **лоадассетс** .</span><span class="sxs-lookup"><span data-stu-id="66eac-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="66eac-117">Обе корневые подписи имеют представление корневого буфера констант (CBV) и таблицу дескриптора представления ресурсов шейдера (SRV).</span><span class="sxs-lookup"><span data-stu-id="66eac-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="66eac-118">У корневой подписи вычислений также есть таблица дескрипторов неупорядоченного представления доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="66eac-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

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



| <span data-ttu-id="66eac-119">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="66eac-119">Call flow</span></span>                                                             | <span data-ttu-id="66eac-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="66eac-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="66eac-121">**\_Диапазон дескрипторов CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="66eac-122">**\_Тип диапазона дескрипторов D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="66eac-123">**\_Корневой \_ параметр CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="66eac-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="66eac-124">**\_Видимость шейдера \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="66eac-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="66eac-125">**\_DESC корневой \_ подписи CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="66eac-126">**\_ \_ Флаги корневой подписи D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="66eac-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="66eac-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="66eac-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="66eac-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="66eac-129">**\_Версия корневой \_ СИГНАТУРы D3D \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="66eac-130">**креатерутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="66eac-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="66eac-131">**\_DESC корневой \_ подписи CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="66eac-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="66eac-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="66eac-133">**\_Версия корневой \_ СИГНАТУРы D3D \_**</span><span class="sxs-lookup"><span data-stu-id="66eac-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="66eac-134">**креатерутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="66eac-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="66eac-135">Создание буферов SRV и UAV</span><span class="sxs-lookup"><span data-stu-id="66eac-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="66eac-136">Буферы SRV и UAV состоят из массива данных о положении и скорости.</span><span class="sxs-lookup"><span data-stu-id="66eac-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

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



| <span data-ttu-id="66eac-137">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="66eac-137">Call flow</span></span>                       | <span data-ttu-id="66eac-138">Параметры</span><span class="sxs-lookup"><span data-stu-id="66eac-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="66eac-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="66eac-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="66eac-140">Создание буферов CBV и вершин</span><span class="sxs-lookup"><span data-stu-id="66eac-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="66eac-141">Для графического конвейера CBV — это **Структура** , содержащая две матрицы, используемые шейдером Geometry.</span><span class="sxs-lookup"><span data-stu-id="66eac-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="66eac-142">Шейдер геометрии берет на себя местоположение каждой части в системе и создает четыре, чтобы представить ее с помощью этих матриц.</span><span class="sxs-lookup"><span data-stu-id="66eac-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

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



| <span data-ttu-id="66eac-143">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="66eac-143">Call flow</span></span>                       | <span data-ttu-id="66eac-144">Параметры</span><span class="sxs-lookup"><span data-stu-id="66eac-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="66eac-145">**ксмматрикс**</span><span class="sxs-lookup"><span data-stu-id="66eac-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="66eac-146">В результате буфер вершин, используемый шейдером вершин, фактически не содержит никаких данных о позиционировании.</span><span class="sxs-lookup"><span data-stu-id="66eac-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="66eac-147">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="66eac-147">Call flow</span></span>                       | <span data-ttu-id="66eac-148">Параметры</span><span class="sxs-lookup"><span data-stu-id="66eac-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="66eac-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="66eac-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="66eac-150">Для конвейера вычислений CBV — это **Структура** , содержащая некоторые константы, используемые симуляцией притяжения в виде «n-Body» в шейдере вычислений.</span><span class="sxs-lookup"><span data-stu-id="66eac-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="66eac-151">Синхронизация потоков отрисовки и вычислений</span><span class="sxs-lookup"><span data-stu-id="66eac-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="66eac-152">После инициализации буферов начнется работа по отрисовке и вычислению.</span><span class="sxs-lookup"><span data-stu-id="66eac-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="66eac-153">Поток вычислений будет изменять состояние двух буферов расположения и скорости между SRV и UAV, так как он выполняет итерацию по моделированию, а потоку отрисовки необходимо убедиться, что он работает над графическим конвейером, который работает с SRV.</span><span class="sxs-lookup"><span data-stu-id="66eac-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="66eac-154">Границы используются для синхронизации доступа к двум буферам.</span><span class="sxs-lookup"><span data-stu-id="66eac-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="66eac-155">В потоке Render:</span><span class="sxs-lookup"><span data-stu-id="66eac-155">On the Render thread:</span></span>

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



| <span data-ttu-id="66eac-156">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="66eac-156">Call flow</span></span>                                                              | <span data-ttu-id="66eac-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="66eac-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="66eac-158">**интерлоккедексчанже**</span><span class="sxs-lookup"><span data-stu-id="66eac-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="66eac-159">**интерлоккеджетвалуе**</span><span class="sxs-lookup"><span data-stu-id="66eac-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="66eac-160">**жеткомплетедвалуе**</span><span class="sxs-lookup"><span data-stu-id="66eac-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="66eac-161">**Ожидание**</span><span class="sxs-lookup"><span data-stu-id="66eac-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="66eac-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="66eac-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="66eac-163">**ексекутекоммандлистс**</span><span class="sxs-lookup"><span data-stu-id="66eac-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="66eac-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="66eac-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="66eac-165">Чтобы упростить пример, поток вычислений ждет завершения каждой итерации GPU, прежде чем планировать дополнительные операции вычислений.</span><span class="sxs-lookup"><span data-stu-id="66eac-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="66eac-166">На практике для достижения максимальной производительности GPU приложения, скорее всего, хотят, чтобы очередь вычислений была заполнена.</span><span class="sxs-lookup"><span data-stu-id="66eac-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="66eac-167">В потоке вычислений:</span><span class="sxs-lookup"><span data-stu-id="66eac-167">On the Compute thread:</span></span>

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



| <span data-ttu-id="66eac-168">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="66eac-168">Call flow</span></span>                                                                   | <span data-ttu-id="66eac-169">Параметры</span><span class="sxs-lookup"><span data-stu-id="66eac-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="66eac-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="66eac-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="66eac-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="66eac-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="66eac-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="66eac-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="66eac-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="66eac-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="66eac-174">**интерлоккеджетвалуе**</span><span class="sxs-lookup"><span data-stu-id="66eac-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="66eac-175">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="66eac-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="66eac-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="66eac-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="66eac-177">**ексекутекоммандлистс**</span><span class="sxs-lookup"><span data-stu-id="66eac-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="66eac-178">**интерлоккединкремент**</span><span class="sxs-lookup"><span data-stu-id="66eac-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="66eac-179">**Имел**</span><span class="sxs-lookup"><span data-stu-id="66eac-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="66eac-180">**сетевентонкомплетион**</span><span class="sxs-lookup"><span data-stu-id="66eac-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="66eac-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="66eac-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="66eac-182">**интерлоккеджетвалуе**</span><span class="sxs-lookup"><span data-stu-id="66eac-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="66eac-183">**жеткомплетедвалуе**</span><span class="sxs-lookup"><span data-stu-id="66eac-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="66eac-184">**Ожидание**</span><span class="sxs-lookup"><span data-stu-id="66eac-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="66eac-185">**интерлоккедексчанже**</span><span class="sxs-lookup"><span data-stu-id="66eac-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="66eac-186">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="66eac-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="66eac-187">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="66eac-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="66eac-188">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="66eac-188">Run the sample</span></span>

![снимок экрана с окончательным моделированием "сила притяжения в тексте"](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="66eac-190">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="66eac-190">Related topics</span></span>

[<span data-ttu-id="66eac-191">Пошаговые инструкции по коду D3D12</span><span class="sxs-lookup"><span data-stu-id="66eac-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="66eac-192">Синхронизация с несколькими модулями</span><span class="sxs-lookup"><span data-stu-id="66eac-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)