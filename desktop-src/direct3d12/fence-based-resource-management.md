---
title: Управление ресурсами на основе границ
description: Показывает, как управлять жизненным циклом данных ресурса путем отслеживания хода выполнения GPU через границы. память можно эффективно повторно использовать с ограждениями, тщательно управляя доступностью свободного пространства в памяти, например в реализации кольцевого буфера для Uploadной кучи.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cbfd9231e3013099c8382072049f1ae1478e28f00830e89fb4ecef1b835ce58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728894"
---
# <a name="fence-based-resource-management"></a>Управление ресурсами на основе границ

Показывает, как управлять жизненным циклом данных ресурса путем отслеживания хода выполнения GPU через границы. память можно эффективно повторно использовать с ограждениями, тщательно управляя доступностью свободного пространства в памяти, например в реализации кольцевого буфера для Uploadной кучи.

-   [Сценарий кольцевого буфера](#ring-buffer-scenario)
-   [Пример кольцевого буфера](#ring-buffer-sample)
-   [Связанные темы](#related-topics)

## <a name="ring-buffer-scenario"></a>Сценарий кольцевого буфера

Ниже приведен пример, в котором приложение сталкивается с редким требованием для отправки динамической памяти.

Кольцевой буфер — это один из способов управления кучей отправки. Кольцевой буфер содержит данные, необходимые для следующих нескольких кадров. Приложение поддерживает текущий указатель ввода данных и очередь со смещением кадров для записи каждого кадра и начальное смещение данных ресурса для этого кадра.

Приложение создает кольцевой буфер, основанный на буфере для передачи данных в GPU для каждого кадра. В настоящее время отображается кадр 2, кольцевой буфер обтекает данные для кадра 4, все данные, необходимые для кадра 5, и большой постоянный буфер, необходимый для кадра 6, должен быть размещен отдельно.

**Рис. 1** . приложение пытается выполнить подраспределение для буфера констант, но находит недостаточно свободной памяти.

![недостаточно свободной памяти в этом кольцевом буфере](images/ring-buffer-1.png)

**Рис. 2** . при опросе ограждения приложение обнаруживает, что кадр 3 был визуализирован, очередь смещений кадров затем обновляется, а текущее состояние кольцевого буфера — тем не менее, свободная память по-прежнему достаточно велика для размещения буфера констант.

![по-прежнему недостаточная память после отрисовки кадра 3](images/ring-buffer-2.png)

**Рис. 3** . при возникновении такой ситуации ЦП блокирует себя (через ограждение в ожидании) до отображения кадра 4, что освобождает память, выделенную для кадра 4.

![подготовка фрейма 4 освобождает больше кольцевого буфера](images/ring-buffer-3.png)

**Рис. 4** . Теперь свободная память достаточно велика для буфера констант и перераспределение выполнена. Приложение копирует данные буфера больших констант в память, ранее используемую данными ресурсов для кадров 3 и 4. В конечном итоге обновляется текущий указатель ввода.

![Теперь имеется комната из кадра 6 в кольцевом буфере](images/ring-buffer-4.png)

Если приложение реализует кольцевой буфер, кольцевой буфер должен быть достаточно большим, чтобы справиться с наиболее серьезным сценарием размеров данных ресурсов.

## <a name="ring-buffer-sample"></a>Пример кольцевого буфера

В следующем примере кода показано, как можно управлять замкнутым кольцевым буфером, обращая внимание на подпрограмму подраспределений, которая обрабатывает опрос ограждения и ожидает ожидания. Для простоты в примере используется недостаточно \_ \_ памяти, чтобы скрыть подробные сведения о недостаточном объеме свободной памяти в куче, поскольку эта логика (на основе *m \_ пдатакур* и смещений внутри *фрамеоффсеткуеуе*) не тесно связана с кучами или ограждениями. Пример упрощен, чтобы пожертвовать частотой кадров вместо использования памяти.

Обратите внимание, что поддержка кольцевых буферов должна быть популярным сценарием. Однако структура кучи не исключает другие способы использования, такие как параметризация списка команд и повторное использование.

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Подраспределение в буферах](large-buffers.md)
</dt> </dl>

 

 




