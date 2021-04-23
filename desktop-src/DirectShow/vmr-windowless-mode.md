---
description: Режим без окон VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Режим без окон VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344372"
---
# <a name="vmr-windowless-mode"></a><span data-ttu-id="acba9-103">Режим без окон VMR</span><span class="sxs-lookup"><span data-stu-id="acba9-103">VMR Windowless Mode</span></span>

<span data-ttu-id="acba9-104">Режим без окон — это предпочтительный способ отображения видео в окне приложения.</span><span class="sxs-lookup"><span data-stu-id="acba9-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="acba9-105">В режиме без окон модуль подготовки видео не загружает свой компонент диспетчера окон и поэтому не поддерживает интерфейсы [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) и [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="acba9-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="acba9-106">Вместо этого приложение предоставляет окно воспроизведения и задает прямоугольник назначения в клиентской области для изображения VMR, чтобы нарисовать видео.</span><span class="sxs-lookup"><span data-stu-id="acba9-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="acba9-107">VMR использует объект DirectDraw Clipper, чтобы убедиться, что видео обрезано в окне приложения и не отображается в других окнах.</span><span class="sxs-lookup"><span data-stu-id="acba9-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="acba9-108">VMR не подклассует окно приложения или устанавливает обработчики систем и процессов.</span><span class="sxs-lookup"><span data-stu-id="acba9-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="acba9-109">В режиме без окон последовательность событий во время соединения и перехода в состояние выполнения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="acba9-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="acba9-110">Вышестоящий фильтр предлагает тип мультимедиа, который VMR принимает или отклоняет.</span><span class="sxs-lookup"><span data-stu-id="acba9-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="acba9-111">Если тип мультимедиа принимается, VMR вызывает средство распределителя-Presenter для получения поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="acba9-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="acba9-112">Если поверхность создана успешно, то контакты соединяются, а фильтр VMR готов к переходу в состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="acba9-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="acba9-113">При запуске графа фильтра декодер вызывает метод " **buffer** " для получения примера мультимедиа из распределителя.</span><span class="sxs-lookup"><span data-stu-id="acba9-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="acba9-114">VMR запрашивает устройство распределителя, чтобы убедиться, что глубина пикселя, размер прямоугольника и другие параметры на поверхности DirectDraw совместимы с входящим видео.</span><span class="sxs-lookup"><span data-stu-id="acba9-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="acba9-115">Если они совместимы, то VMR возвращает для декодера поверхность DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="acba9-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="acba9-116">После декодирования декодера в области основной модуль синхронизации VMR проверяет отметки времени.</span><span class="sxs-lookup"><span data-stu-id="acba9-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="acba9-117">Эта единица блокирует вызов **Receive** до наступления времени презентации.</span><span class="sxs-lookup"><span data-stu-id="acba9-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="acba9-118">На этом этапе VMR вызывает **пресентимаже** для распределителя-Presenter, который представляет поверхность для графической карты.</span><span class="sxs-lookup"><span data-stu-id="acba9-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="acba9-119">На следующем рисунке показан фильтр VMR в режиме без окон с несколькими входными потоками.</span><span class="sxs-lookup"><span data-stu-id="acba9-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![VMR в режиме без окон](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="acba9-121">**Настройка VMR-7 для режима без окон**</span><span class="sxs-lookup"><span data-stu-id="acba9-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="acba9-122">Чтобы настроить VMR-7 для режима без окон, перед подключением любых входных ПИН-кодов VMR выполните все описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="acba9-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="acba9-123">Создайте фильтр и добавьте его в граф.</span><span class="sxs-lookup"><span data-stu-id="acba9-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="acba9-124">Вызовите метод [**ивмрфилтерконфиг:: сетрендерингмоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) с \_ неоконным флагом вмрмоде.</span><span class="sxs-lookup"><span data-stu-id="acba9-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="acba9-125">При необходимости настройте VMR для нескольких входных потоков, вызвав [**ивмрфилтерконфиг:: сетнумберофстреамс**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="acba9-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="acba9-126">VMR создает ПИН-код входа для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="acba9-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="acba9-127">Используйте интерфейс [**ивмрмиксерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) , чтобы задать Z-порядок и другие параметры для потока.</span><span class="sxs-lookup"><span data-stu-id="acba9-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="acba9-128">Дополнительные сведения см. [в разделе VMR с несколькими потоками (режим смешения)](vmr-with-multiple-streams--mixing-mode.md).</span><span class="sxs-lookup"><span data-stu-id="acba9-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="acba9-129">Если не вызвать **сетнумберофстреамс**, VMR-7 по умолчанию принимает один входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="acba9-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="acba9-130">После подключения входных контактов число ПИН-кодов не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="acba9-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="acba9-131">Вызовите метод [**ивмрвиндовлессконтрол:: сетвидеоклиппингвиндов**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) , чтобы указать окно, в котором будет отображаться отображаемое видео.</span><span class="sxs-lookup"><span data-stu-id="acba9-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="acba9-132">После выполнения этих действий можно подключить входные сигналы фильтра VMR.</span><span class="sxs-lookup"><span data-stu-id="acba9-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="acba9-133">Существует несколько способов создания графа, таких как соединение закрепления напрямую, с помощью интеллектуальных методов соединения, таких как [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), или с помощью метода [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) построителя Graph.</span><span class="sxs-lookup"><span data-stu-id="acba9-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="acba9-134">Дополнительные сведения см. в разделе [общие Graph-Building методы](general-graph-building-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="acba9-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="acba9-135">Чтобы задать расположение видео в окне приложения, вызовите метод [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="acba9-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="acba9-136">Метод [**ивмрвиндовлессконтрол:: жетнативевидеосизе**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) возвращает собственный размер видео.</span><span class="sxs-lookup"><span data-stu-id="acba9-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="acba9-137">Во время воспроизведения приложение должно уведомлять VMR о следующих сообщениях Windows:</span><span class="sxs-lookup"><span data-stu-id="acba9-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="acba9-138">WM \_ Paint: вызов [**ивмрвиндовлессконтрол:: репаинтвидео**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) для перерисовки изображения.</span><span class="sxs-lookup"><span data-stu-id="acba9-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="acba9-139">WM \_ дисплайчанже: Call [**ивмрвиндовлессконтрол::D исплаймодечанжед**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="acba9-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="acba9-140">VMR выполняет все действия, необходимые для показа видео с новым разрешением или глубиной цвета.</span><span class="sxs-lookup"><span data-stu-id="acba9-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="acba9-141">Размер WM: повторное \_ Вычисление расположения видео и вызов [**сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) при необходимости.</span><span class="sxs-lookup"><span data-stu-id="acba9-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="acba9-142">Приложения MFC должны определять пустой \_ обработчик сообщений WM ерасебкгнд, иначе область видеоизображения не будет правильно перерисовываться.</span><span class="sxs-lookup"><span data-stu-id="acba9-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="acba9-143">**Настройка VMR-9 для режима без окон**</span><span class="sxs-lookup"><span data-stu-id="acba9-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="acba9-144">Чтобы настроить VMR-9 для режима без окон, выполните действия, описанные в разделе VMR-7 для режима без окон, но используйте интерфейсы [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) и [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="acba9-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="acba9-145">Единственная существенная разница заключается в том, что VMR-9 создает четыре входных контакта по умолчанию, а не один входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="acba9-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="acba9-146">Поэтому необходимо вызвать **сетнумберофстреамс** только в том случае, если используется более четырех потоков видео.</span><span class="sxs-lookup"><span data-stu-id="acba9-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="acba9-147">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="acba9-147">**Example Code**</span></span>

<span data-ttu-id="acba9-148">В следующем коде показано, как создать фильтр VMR-7, добавить его в граф фильтра DirectShow, а затем перевести VMR в режим без окон.</span><span class="sxs-lookup"><span data-stu-id="acba9-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="acba9-149">Для VMR-9 используйте CLSID \_ VideoMixingRenderer9 в **CoCreateInstance** и соответствующие интерфейсы VMR-9.</span><span class="sxs-lookup"><span data-stu-id="acba9-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="acba9-150">См. также</span><span class="sxs-lookup"><span data-stu-id="acba9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acba9-151">Использование режима без окон</span><span class="sxs-lookup"><span data-stu-id="acba9-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



