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
# <a name="desktop-duplication-api"></a><span data-ttu-id="3136c-103">API дублирования рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-103">Desktop Duplication API</span></span>

<span data-ttu-id="3136c-104">Windows 8 отключает стандартные драйверы зеркального отображения Windows 2000 и предлагает API дублирования настольных систем.</span><span class="sxs-lookup"><span data-stu-id="3136c-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="3136c-105">API дублирования настольных систем обеспечивает удаленный доступ к образу рабочего стола для сценариев совместной работы.</span><span class="sxs-lookup"><span data-stu-id="3136c-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="3136c-106">Приложения могут использовать API дублирования настольных систем для доступа к покадровым обновлениям на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="3136c-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="3136c-107">Так как приложения получают обновления для образа рабочего стола на поверхности DXGI, приложения могут использовать все возможности GPU для обработки обновлений образов.</span><span class="sxs-lookup"><span data-stu-id="3136c-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="3136c-108">Обновление данных образа рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="3136c-109">Поворот образа рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="3136c-110">Обновление указателя рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="3136c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="3136c-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="3136c-112">Обновление данных образа рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-112">Updating the desktop image data</span></span>

<span data-ttu-id="3136c-113">DXGI предоставляет поверхность, которая содержит текущий образ рабочего стола с помощью нового метода [**идксгиаутпутдупликатион:: аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) .</span><span class="sxs-lookup"><span data-stu-id="3136c-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="3136c-114">Формат образа рабочего стола всегда имеет [**\_ Формат DXGI \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) независимо от текущего режима экрана.</span><span class="sxs-lookup"><span data-stu-id="3136c-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="3136c-115">Вместе с этой поверхностью эти методы [**идксгиаутпутдупликатион**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) возвращают указанные типы сведений, которые помогут определить, какие пиксели в поверхности нужно обработать:</span><span class="sxs-lookup"><span data-stu-id="3136c-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="3136c-116">[**Идксгиаутпутдупликатион:: жетфрамедиртиректс**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) возвращает "грязные" регионы, которые являются перекрывающимися прямоугольниками, которые указывают области образа рабочего стола, обновленные операционной системой с момента обработки предыдущего образа рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3136c-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="3136c-117">[**Идксгиаутпутдупликатион:: жетфрамемоверектс**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) возвращает регионы перемещения, которые представляют собой прямоугольники пикселов в образе рабочего стола, которые операционная система переместила в другое расположение в том же образе.</span><span class="sxs-lookup"><span data-stu-id="3136c-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="3136c-118">Каждая область перемещения состоит из прямоугольника назначения и исходной точки.</span><span class="sxs-lookup"><span data-stu-id="3136c-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="3136c-119">Исходная точка указывает расположение, из которого операционная система скопировала регион и прямоугольник назначения указывает, где операционная система переместила этот регион.</span><span class="sxs-lookup"><span data-stu-id="3136c-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="3136c-120">Области перемещения всегда являются нерастяжениями, поэтому источник всегда имеет тот же размер, что и назначение.</span><span class="sxs-lookup"><span data-stu-id="3136c-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="3136c-121">Предположим, что образ настольного компьютера был передан через низкое подключение к удаленному клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="3136c-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="3136c-122">Объем данных, передаваемых через соединение, сокращается за счет получения только данных о том, как ваше клиентское приложение должно перемещать области пикселей, а не данные о фактических данных пикселей.</span><span class="sxs-lookup"><span data-stu-id="3136c-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="3136c-123">Для обработки перемещений клиентское приложение должно сохранить полный образ последнего образа.</span><span class="sxs-lookup"><span data-stu-id="3136c-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="3136c-124">Хотя операционная система накапливает необработанные обновления образов настольных систем, для точного хранения регионов обновления может не хватает свободного пространства.</span><span class="sxs-lookup"><span data-stu-id="3136c-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="3136c-125">В этом случае операционная система начинает накапливать обновления, объединяя их с существующими регионами обновления для покрытия всех новых обновлений.</span><span class="sxs-lookup"><span data-stu-id="3136c-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="3136c-126">В результате операционная система охватывает пикселы, которые она пока не обновляла в этой рамке.</span><span class="sxs-lookup"><span data-stu-id="3136c-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="3136c-127">Но эта ситуация не создает визуальных проблем в клиентском приложении, так как вы получаете весь образ рабочего стола, а не только обновленные Пиксели.</span><span class="sxs-lookup"><span data-stu-id="3136c-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="3136c-128">Для восстановления правильного образа рабочего стола клиентское приложение должно сначала обработать все регионы перемещения, а затем обработать все изменившиеся регионы.</span><span class="sxs-lookup"><span data-stu-id="3136c-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="3136c-129">Один из этих списков «грязных» и «перемещаемых» областей может быть полностью пустым.</span><span class="sxs-lookup"><span data-stu-id="3136c-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="3136c-130">В примере кода из [примера дублирования рабочего стола](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) показано, как обрабатывать как изменившиеся, так и перемещенные области в одном кадре:</span><span class="sxs-lookup"><span data-stu-id="3136c-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


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



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="3136c-131">Поворот образа рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-131">Rotating the desktop image</span></span>

<span data-ttu-id="3136c-132">Необходимо добавить явный код в клиентское приложение для дублирования настольных систем для поддержки повернутых режимов.</span><span class="sxs-lookup"><span data-stu-id="3136c-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="3136c-133">В повернутом режиме поверхность, полученная от [**идксгиаутпутдупликатион:: аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) , всегда находится на ориентации без вращения, а изображение настольного компьютера поворачивается на поверхности.</span><span class="sxs-lookup"><span data-stu-id="3136c-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="3136c-134">Например, если для рабочего стола задано значение 768x1024 при повороте на 90 градусов, **аккуиренекстфраме** возвращает область 1024x768 с изображением рабочего стола, повернутым в него.</span><span class="sxs-lookup"><span data-stu-id="3136c-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="3136c-135">Ниже приведены некоторые примеры ротации.</span><span class="sxs-lookup"><span data-stu-id="3136c-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="3136c-136">Режим экрана, заданный в панели управления экрана</span><span class="sxs-lookup"><span data-stu-id="3136c-136">Display mode set from display control panel</span></span> | <span data-ttu-id="3136c-137">Режим вывода, возвращаемый GDI или DXGI</span><span class="sxs-lookup"><span data-stu-id="3136c-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="3136c-138">Поверхность, возвращенная из [ **аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="3136c-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3136c-139">ландшафт (1024x768)</span><span class="sxs-lookup"><span data-stu-id="3136c-139">1024x768 landscape</span></span>                          | <span data-ttu-id="3136c-140">поворот на 1024x768 0 градусов</span><span class="sxs-lookup"><span data-stu-id="3136c-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="3136c-141">\[символ новой строки 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="3136c-141">1024x768\[newline\]</span></span> ![повернутый удаленный рабочий стол](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="3136c-143">1024x768 портрет</span><span class="sxs-lookup"><span data-stu-id="3136c-143">1024x768 portrait</span></span>                           | <span data-ttu-id="3136c-144">вращение градуса 768x1024 90</span><span class="sxs-lookup"><span data-stu-id="3136c-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="3136c-145">\[символ новой строки 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="3136c-145">1024x768\[newline\]</span></span> ![Удаленный рабочий стол с поворотом на 90 градусов](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="3136c-147">1024x768 (с отражением)</span><span class="sxs-lookup"><span data-stu-id="3136c-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="3136c-148">поворот на 1024x768 180 градусов</span><span class="sxs-lookup"><span data-stu-id="3136c-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="3136c-149">\[символ новой строки 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="3136c-149">1024x768\[newline\]</span></span> ![Удаленный рабочий стол с поворотом на 180 градусов](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="3136c-151">1024x768 (с отражением)</span><span class="sxs-lookup"><span data-stu-id="3136c-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="3136c-152">вращение градуса 768x1024 270</span><span class="sxs-lookup"><span data-stu-id="3136c-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="3136c-153">\[символ новой строки 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="3136c-153">1024x768\[newline\]</span></span> ![Удаленный рабочий стол с поворотом на 270 градусов](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="3136c-155">Код в клиентском приложении для дублирования настольных систем должен соответствующим образом повернуть образ рабочего стола перед отображением образа рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3136c-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="3136c-156">В сценариях с несколькими мониторами можно поворачивать образ рабочего стола для каждого монитора независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="3136c-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="3136c-157">Обновление указателя рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3136c-157">Updating the desktop pointer</span></span>

<span data-ttu-id="3136c-158">Необходимо использовать API дублирования настольных систем, чтобы определить, должна ли клиентское приложение нарисовать фигуру указателя мыши на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="3136c-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="3136c-159">Либо указатель мыши уже нарисован на рабочем столе, который [**идксгиаутпутдупликатион:: аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) предоставляет, либо указатель мыши отделен от образа рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3136c-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="3136c-160">Если указатель мыши рисуется на рабочем столе, данные о положении указателя, сообщаемые **аккуиренекстфраме** (в элементе **поинтерпоситион** в [**DXGI \_ аутдупл \_ \_ сведения о кадре**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) , на который указывает параметр *пфрамеинфо* ), указывают на то, что отдельный указатель не виден.</span><span class="sxs-lookup"><span data-stu-id="3136c-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="3136c-161">Если графический адаптер накладывает указатель мыши над изображением рабочего стола, **аккуиренекстфраме** сообщает, что виден отдельный указатель.</span><span class="sxs-lookup"><span data-stu-id="3136c-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="3136c-162">Таким образом, клиентское приложение должно нарисовать фигуру указателя мыши на рабочем столе, чтобы точно представить, что текущий пользователь увидит на мониторе.</span><span class="sxs-lookup"><span data-stu-id="3136c-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="3136c-163">Чтобы нарисовать указатель мыши на настольной системе, используйте элемент **поинтерпоситион** в [**\_ \_ \_ сведениях о кадре DXGI аутдупл**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) из параметра *пфрамеинфо* [**аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) , чтобы определить расположение верхнего левого угла указателя мыши в образе рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="3136c-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="3136c-164">При рисовании первого кадра необходимо использовать метод [**идксгиаутпутдупликатион:: жетфрамепоинтершапе**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) для получения сведений о форме указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="3136c-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="3136c-165">Каждый вызов **аккуиренекстфраме** для получения следующего кадра также предоставляет текущую позиции указателя для этого кадра.</span><span class="sxs-lookup"><span data-stu-id="3136c-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="3136c-166">С другой стороны, необходимо использовать **жетфрамепоинтершапе** повторно только при изменении фигуры.</span><span class="sxs-lookup"><span data-stu-id="3136c-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="3136c-167">Итак, скопируйте копию последнего изображения указателя и используйте его для рисования на рабочем столе, если только форма указателя мыши не изменилась.</span><span class="sxs-lookup"><span data-stu-id="3136c-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="3136c-168">Вместе с изображением фигуры указателя [**жетфрамепоинтершапе**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) предоставляет размер места расположения горячей точки.</span><span class="sxs-lookup"><span data-stu-id="3136c-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="3136c-169">Активная разактивная информация предоставляется только в информационных целях.</span><span class="sxs-lookup"><span data-stu-id="3136c-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="3136c-170">Расположение для рисования изображения указателя не зависит от активной области.</span><span class="sxs-lookup"><span data-stu-id="3136c-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="3136c-171">В этом примере кода из [примера дублирования рабочего стола](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) показано, как получить форму указателя мыши:</span><span class="sxs-lookup"><span data-stu-id="3136c-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3136c-172">См. также</span><span class="sxs-lookup"><span data-stu-id="3136c-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3136c-173">Усовершенствования DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="3136c-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
