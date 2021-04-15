---
description: Windows 8 отключает стандартные драйверы зеркального отображения Windows 2000 и предлагает API дублирования настольных систем.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API дублирования рабочего стола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494562"
---
# <a name="desktop-duplication-api"></a>API дублирования рабочего стола

Windows 8 отключает стандартные драйверы зеркального отображения Windows 2000 и предлагает API дублирования настольных систем. API дублирования настольных систем обеспечивает удаленный доступ к образу рабочего стола для сценариев совместной работы. Приложения могут использовать API дублирования настольных систем для доступа к покадровым обновлениям на рабочем столе. Так как приложения получают обновления для образа рабочего стола на поверхности DXGI, приложения могут использовать все возможности GPU для обработки обновлений образов.

-   [Обновление данных образа рабочего стола](#updating-the-desktop-image-data)
-   [Поворот образа рабочего стола](#rotating-the-desktop-image)
-   [Обновление указателя рабочего стола](#updating-the-desktop-pointer)
-   [См. также](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Обновление данных образа рабочего стола

DXGI предоставляет поверхность, которая содержит текущий образ рабочего стола с помощью нового метода [**идксгиаутпутдупликатион:: аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) . Формат образа рабочего стола всегда имеет [**\_ Формат DXGI \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) независимо от текущего режима экрана. Вместе с этой поверхностью эти методы [**идксгиаутпутдупликатион**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) возвращают указанные типы сведений, которые помогут определить, какие пиксели в поверхности нужно обработать:

-   [**Идксгиаутпутдупликатион:: жетфрамедиртиректс**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) возвращает "грязные" регионы, которые являются перекрывающимися прямоугольниками, которые указывают области образа рабочего стола, обновленные операционной системой с момента обработки предыдущего образа рабочего стола.
-   [**Идксгиаутпутдупликатион:: жетфрамемоверектс**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) возвращает регионы перемещения, которые представляют собой прямоугольники пикселов в образе рабочего стола, которые операционная система переместила в другое расположение в том же образе. Каждая область перемещения состоит из прямоугольника назначения и исходной точки. Исходная точка указывает расположение, из которого операционная система скопировала регион и прямоугольник назначения указывает, где операционная система переместила этот регион. Области перемещения всегда являются нерастяжениями, поэтому источник всегда имеет тот же размер, что и назначение.

Предположим, что образ настольного компьютера был передан через низкое подключение к удаленному клиентскому приложению. Объем данных, передаваемых через соединение, сокращается за счет получения только данных о том, как ваше клиентское приложение должно перемещать области пикселей, а не данные о фактических данных пикселей. Для обработки перемещений клиентское приложение должно сохранить полный образ последнего образа.

Хотя операционная система накапливает необработанные обновления образов настольных систем, для точного хранения регионов обновления может не хватает свободного пространства. В этом случае операционная система начинает накапливать обновления, объединяя их с существующими регионами обновления для покрытия всех новых обновлений. В результате операционная система охватывает пикселы, которые она пока не обновляла в этой рамке. Но эта ситуация не создает визуальных проблем в клиентском приложении, так как вы получаете весь образ рабочего стола, а не только обновленные Пиксели.

Для восстановления правильного образа рабочего стола клиентское приложение должно сначала обработать все регионы перемещения, а затем обработать все изменившиеся регионы. Один из этих списков «грязных» и «перемещаемых» областей может быть полностью пустым. В примере кода из [примера дублирования рабочего стола](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) показано, как обрабатывать как изменившиеся, так и перемещенные области в одном кадре:


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a>Поворот образа рабочего стола

Необходимо добавить явный код в клиентское приложение для дублирования настольных систем для поддержки повернутых режимов. В повернутом режиме поверхность, полученная от [**идксгиаутпутдупликатион:: аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) , всегда находится на ориентации без вращения, а изображение настольного компьютера поворачивается на поверхности. Например, если для рабочего стола задано значение 768x1024 при повороте на 90 градусов, **аккуиренекстфраме** возвращает область 1024x768 с изображением рабочего стола, повернутым в него. Ниже приведены некоторые примеры ротации.



| Режим экрана, заданный в панели управления экрана | Режим вывода, возвращаемый GDI или DXGI | Поверхность, возвращенная из [ **аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| ландшафт (1024x768)                          | поворот на 1024x768 0 градусов           | \[символ новой строки 1024x768\] ![повернутый удаленный рабочий стол](images/dxgi-outdupl-0-rotate.png)<br/>            |
| 1024x768 портрет                           | вращение градуса 768x1024 90          | \[символ новой строки 1024x768\] ![Удаленный рабочий стол с поворотом на 90 градусов](images/dxgi-outdupl-90-rotate.png)<br/>   |
| 1024x768 (с отражением)                | поворот на 1024x768 180 градусов         | \[символ новой строки 1024x768\] ![Удаленный рабочий стол с поворотом на 180 градусов](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024x768 (с отражением)                 | вращение градуса 768x1024 270         | \[символ новой строки 1024x768\] ![Удаленный рабочий стол с поворотом на 270 градусов](images/dxgi-outdupl-270-rotate.png)<br/> |



 

Код в клиентском приложении для дублирования настольных систем должен соответствующим образом повернуть образ рабочего стола перед отображением образа рабочего стола.

> [!Note]  
> В сценариях с несколькими мониторами можно поворачивать образ рабочего стола для каждого монитора независимо друг от друга.

 

## <a name="updating-the-desktop-pointer"></a>Обновление указателя рабочего стола

Необходимо использовать API дублирования настольных систем, чтобы определить, должна ли клиентское приложение нарисовать фигуру указателя мыши на рабочем столе. Либо указатель мыши уже нарисован на рабочем столе, который [**идксгиаутпутдупликатион:: аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) предоставляет, либо указатель мыши отделен от образа рабочего стола. Если указатель мыши рисуется на рабочем столе, данные о положении указателя, сообщаемые **аккуиренекстфраме** (в элементе **поинтерпоситион** в [**DXGI \_ аутдупл \_ \_ сведения о кадре**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) , на который указывает параметр *пфрамеинфо* ), указывают на то, что отдельный указатель не виден. Если графический адаптер накладывает указатель мыши над изображением рабочего стола, **аккуиренекстфраме** сообщает, что виден отдельный указатель. Таким образом, клиентское приложение должно нарисовать фигуру указателя мыши на рабочем столе, чтобы точно представить, что текущий пользователь увидит на мониторе.

Чтобы нарисовать указатель мыши на настольной системе, используйте элемент **поинтерпоситион** в [**\_ \_ \_ сведениях о кадре DXGI аутдупл**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) из параметра *пфрамеинфо* [**аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) , чтобы определить расположение верхнего левого угла указателя мыши в образе рабочего стола. При рисовании первого кадра необходимо использовать метод [**идксгиаутпутдупликатион:: жетфрамепоинтершапе**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) для получения сведений о форме указателя мыши. Каждый вызов **аккуиренекстфраме** для получения следующего кадра также предоставляет текущую позиции указателя для этого кадра. С другой стороны, необходимо использовать **жетфрамепоинтершапе** повторно только при изменении фигуры. Итак, скопируйте копию последнего изображения указателя и используйте его для рисования на рабочем столе, если только форма указателя мыши не изменилась.

> [!Note]  
> Вместе с изображением фигуры указателя [**жетфрамепоинтершапе**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) предоставляет размер места расположения горячей точки. Активная разактивная информация предоставляется только в информационных целях. Расположение для рисования изображения указателя не зависит от активной области.

 

В этом примере кода из [примера дублирования рабочего стола](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) показано, как получить форму указателя мыши:


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Усовершенствования DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
