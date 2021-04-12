---
description: Просмотр стандартного телетекста в мире
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Просмотр стандартного телетекста в мире
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344375"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="7421c-103">Просмотр стандартного телетекста в мире</span><span class="sxs-lookup"><span data-stu-id="7421c-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="7421c-104">Эта функция была удалена из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="7421c-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="7421c-105">Он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7421c-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="7421c-106">Международный стандарт телетекста (WST) кодируется в вертикальном интервале (ВБИ) аналогового телевизионного сигнала.</span><span class="sxs-lookup"><span data-stu-id="7421c-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="7421c-107">Граф фильтра для предварительного просмотра телетекста аналогичен графу, используемому для просмотра скрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="7421c-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="7421c-108">Эта диаграмма показана на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="7421c-108">The following diagram illustrates this graph.</span></span>

![Диаграмма WST Preview](images/vidcap10.png)

<span data-ttu-id="7421c-110">Эта диаграмма использует следующие фильтры для отображения WST:</span><span class="sxs-lookup"><span data-stu-id="7421c-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="7421c-111">[Преобразователь tee/Sink-to-Sink](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="7421c-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="7421c-112">Принимает сведения ВБИ из фильтра записи и разделяет их на отдельные потоки для каждой из служб данных, имеющихся в сигнале.</span><span class="sxs-lookup"><span data-stu-id="7421c-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="7421c-113">[WST кодек](wst-codec-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7421c-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="7421c-114">Декодирует данные телетекста из примеров ВБИ.</span><span class="sxs-lookup"><span data-stu-id="7421c-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="7421c-115">[WST декодер](wst-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7421c-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="7421c-116">Преобразует данные телетекста и рисует текст на точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="7421c-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="7421c-117">Нисходящий фильтр (в данном случае микшер наложения) накладывает на видео растровые изображения.</span><span class="sxs-lookup"><span data-stu-id="7421c-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="7421c-118">Метод **RenderStream** в построителе графов записи не поддерживает фильтры WST напрямую, поэтому приложение должно выполнить некоторую дополнительную работу.</span><span class="sxs-lookup"><span data-stu-id="7421c-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="7421c-119">Добавьте фильтр микшера наложения к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="7421c-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="7421c-120">В следующем коде используется функция Аддфилтербиклсид, описанная в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="7421c-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="7421c-121">(Аддфилтербиклсид не является API DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="7421c-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="7421c-122">Подключите предварительный ПИН-код к фильтру модуля подготовки видео с помощью микшера наложения.</span><span class="sxs-lookup"><span data-stu-id="7421c-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="7421c-123">Метод **RenderStream** можно использовать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7421c-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="7421c-124">Добавьте фильтр преобразователя tee/Sink-to-Sink в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="7421c-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="7421c-125">В следующем коде используется функция Креатекернелфилтер, описанная в разделе [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7421c-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="7421c-126">(Креатекернелфилтер не является API DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="7421c-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="7421c-127">Добавьте фильтр кодека WST в граф фильтра:</span><span class="sxs-lookup"><span data-stu-id="7421c-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="7421c-128">Вызовите **RenderStream** , чтобы подключить ПИН-код ВБИ фильтра захвата к преобразовательу tee/Sink-Sink, а также к преобразователю tee/Sink-Sink в фильтре кодека WST:</span><span class="sxs-lookup"><span data-stu-id="7421c-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="7421c-129">Вызовите **RenderStream** еще раз, чтобы подключить фильтр кодека WST к микшеру наложения.</span><span class="sxs-lookup"><span data-stu-id="7421c-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="7421c-130">Фильтр декодера WST автоматически помещается в граф.</span><span class="sxs-lookup"><span data-stu-id="7421c-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="7421c-131">Не забудьте освободить все интерфейсы фильтров.</span><span class="sxs-lookup"><span data-stu-id="7421c-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="7421c-132">В настоящее время фильтр WST декодера не поддерживает подключения к фильтру модуля подготовки видео (VMR).</span><span class="sxs-lookup"><span data-stu-id="7421c-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="7421c-133">Поэтому для просмотра телетекста необходимо использовать фильтр модуля подготовки видео прежних версий.</span><span class="sxs-lookup"><span data-stu-id="7421c-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="7421c-134">Если фильтр записи имеет ПИН-код ВБИ (ПИН-код \_ категпори \_ видеопорт \_ ВБИ), подключите его к фильтру [распределителя (ВБИ Surface](vbi-surface-allocator.md) ).</span><span class="sxs-lookup"><span data-stu-id="7421c-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="7421c-135">В противном случае граф будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="7421c-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="7421c-136">В следующем примере кода используется функция Аддфилтербиклсид, описанная в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md), и функция финдпинбикатегори, описанная в разделе [Работа с категориями ПИН-кода](working-with-pin-categories.md).</span><span class="sxs-lookup"><span data-stu-id="7421c-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="7421c-137">(Ни одна из функций не является API DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="7421c-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="7421c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7421c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7421c-139">Субтитры и телетекст</span><span class="sxs-lookup"><span data-stu-id="7421c-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



