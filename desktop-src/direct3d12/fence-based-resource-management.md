---
title: Управление ресурсами Fence-Based
description: Показывает, как управлять жизненным циклом данных ресурса путем отслеживания хода выполнения GPU через границы. Память можно эффективно повторно использовать с ограждениями, тщательно управляя доступностью свободного пространства в памяти, например в реализации кольцевого буфера для отправки кучи.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104182"
---
# <a name="fence-based-resource-management"></a><span data-ttu-id="1c235-104">Управление ресурсами Fence-Based</span><span class="sxs-lookup"><span data-stu-id="1c235-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="1c235-105">Показывает, как управлять жизненным циклом данных ресурса путем отслеживания хода выполнения GPU через границы.</span><span class="sxs-lookup"><span data-stu-id="1c235-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="1c235-106">Память можно эффективно повторно использовать с ограждениями, тщательно управляя доступностью свободного пространства в памяти, например в реализации кольцевого буфера для отправки кучи.</span><span class="sxs-lookup"><span data-stu-id="1c235-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="1c235-107">Сценарий кольцевого буфера</span><span class="sxs-lookup"><span data-stu-id="1c235-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="1c235-108">Пример кольцевого буфера</span><span class="sxs-lookup"><span data-stu-id="1c235-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="1c235-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1c235-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="1c235-110">Сценарий кольцевого буфера</span><span class="sxs-lookup"><span data-stu-id="1c235-110">Ring buffer scenario</span></span>

<span data-ttu-id="1c235-111">Ниже приведен пример, в котором приложение сталкивается с редким требованием для отправки динамической памяти.</span><span class="sxs-lookup"><span data-stu-id="1c235-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="1c235-112">Кольцевой буфер — это один из способов управления кучей отправки.</span><span class="sxs-lookup"><span data-stu-id="1c235-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="1c235-113">Кольцевой буфер содержит данные, необходимые для следующих нескольких кадров.</span><span class="sxs-lookup"><span data-stu-id="1c235-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="1c235-114">Приложение поддерживает текущий указатель ввода данных и очередь со смещением кадров для записи каждого кадра и начальное смещение данных ресурса для этого кадра.</span><span class="sxs-lookup"><span data-stu-id="1c235-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="1c235-115">Приложение создает кольцевой буфер, основанный на буфере для передачи данных в GPU для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="1c235-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="1c235-116">В настоящее время отображается кадр 2, кольцевой буфер обтекает данные для кадра 4, все данные, необходимые для кадра 5, и большой постоянный буфер, необходимый для кадра 6, должен быть размещен отдельно.</span><span class="sxs-lookup"><span data-stu-id="1c235-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="1c235-117">**Рис. 1** . приложение пытается выполнить подраспределение для буфера констант, но находит недостаточно свободной памяти.</span><span class="sxs-lookup"><span data-stu-id="1c235-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![недостаточно свободной памяти в этом кольцевом буфере](images/ring-buffer-1.png)

<span data-ttu-id="1c235-119">**Рис. 2** . при опросе ограждения приложение обнаруживает, что кадр 3 был визуализирован, очередь смещений кадров затем обновляется, а текущее состояние кольцевого буфера — тем не менее, свободная память по-прежнему достаточно велика для размещения буфера констант.</span><span class="sxs-lookup"><span data-stu-id="1c235-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![по-прежнему недостаточная память после отрисовки кадра 3](images/ring-buffer-2.png)

<span data-ttu-id="1c235-121">**Рис. 3** . при возникновении такой ситуации ЦП блокирует себя (через ограждение в ожидании) до отображения кадра 4, что освобождает память, выделенную для кадра 4.</span><span class="sxs-lookup"><span data-stu-id="1c235-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![подготовка фрейма 4 освобождает больше кольцевого буфера](images/ring-buffer-3.png)

<span data-ttu-id="1c235-123">**Рис. 4** . Теперь свободная память достаточно велика для буфера констант и перераспределение выполнена. Приложение копирует данные буфера больших констант в память, ранее используемую данными ресурсов для кадров 3 и 4.</span><span class="sxs-lookup"><span data-stu-id="1c235-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="1c235-124">В конечном итоге обновляется текущий указатель ввода.</span><span class="sxs-lookup"><span data-stu-id="1c235-124">The current input pointer is finally updated.</span></span>

![Теперь имеется комната из кадра 6 в кольцевом буфере](images/ring-buffer-4.png)

<span data-ttu-id="1c235-126">Если приложение реализует кольцевой буфер, кольцевой буфер должен быть достаточно большим, чтобы справиться с наиболее серьезным сценарием размеров данных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c235-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="1c235-127">Пример кольцевого буфера</span><span class="sxs-lookup"><span data-stu-id="1c235-127">Ring buffer sample</span></span>

<span data-ttu-id="1c235-128">В следующем примере кода показано, как можно управлять замкнутым кольцевым буфером, обращая внимание на подпрограмму подраспределений, которая обрабатывает опрос ограждения и ожидает ожидания.</span><span class="sxs-lookup"><span data-stu-id="1c235-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="1c235-129">Для простоты в примере используется недостаточно \_ \_ памяти, чтобы скрыть подробные сведения о недостаточном объеме свободной памяти в куче, поскольку эта логика (на основе *m \_ пдатакур* и смещений внутри *фрамеоффсеткуеуе*) не тесно связана с кучами или ограждениями.</span><span class="sxs-lookup"><span data-stu-id="1c235-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="1c235-130">Пример упрощен, чтобы пожертвовать частотой кадров вместо использования памяти.</span><span class="sxs-lookup"><span data-stu-id="1c235-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="1c235-131">Обратите внимание, что поддержка кольцевых буферов должна быть популярным сценарием. Однако структура кучи не исключает другие способы использования, такие как параметризация списка команд и повторное использование.</span><span class="sxs-lookup"><span data-stu-id="1c235-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="1c235-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1c235-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c235-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="1c235-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="1c235-134">Подраспределение в буферах</span><span class="sxs-lookup"><span data-stu-id="1c235-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




