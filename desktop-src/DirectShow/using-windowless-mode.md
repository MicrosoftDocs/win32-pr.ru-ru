---
description: Использование режима без окон
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Использование режима без окон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911067"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="b1e09-103">Использование режима без окон</span><span class="sxs-lookup"><span data-stu-id="b1e09-103">Using Windowless Mode</span></span>

<span data-ttu-id="b1e09-104">Оба фильтра модуля подготовки [видео](video-mixing-renderer-filter-7.md) (VMR-7) и i [микширования видео с фильтром 9](video-mixing-renderer-filter-9.md) (VMR-9) поддерживают *безоконный режим*, что представляет собой значительное улучшение по сравнению с интерфейсом [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="b1e09-105">В этом разделе описываются различия между режимом без окон и оконным режимом, а также использование режима без окон.</span><span class="sxs-lookup"><span data-stu-id="b1e09-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="b1e09-106">Чтобы сохранить обратную совместимость с существующими приложениями, параметр VMR по умолчанию имеет режим окон.</span><span class="sxs-lookup"><span data-stu-id="b1e09-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="b1e09-107">В оконном режиме модуль подготовки отчетов создает собственное окно для отображения видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="b1e09-108">Как правило, приложение устанавливает, что окно видео является дочерним по отношению к окну приложения.</span><span class="sxs-lookup"><span data-stu-id="b1e09-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="b1e09-109">Наличие отдельного окна видео вызывает некоторые проблемы.</span><span class="sxs-lookup"><span data-stu-id="b1e09-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="b1e09-110">Что важнее всего, существует вероятность возникновения взаимоблокировок при отправке сообщений окна между потоками.</span><span class="sxs-lookup"><span data-stu-id="b1e09-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="b1e09-111">Диспетчер графов фильтров должен пересылать определенные окна сообщений, например WM \_ Paint, в модуль подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="b1e09-112">Приложение должно использовать реализацию [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) для диспетчера графа фильтров (а не для модуля подготовки видео), чтобы диспетчер графа фильтров сохранит правильное внутреннее состояние.</span><span class="sxs-lookup"><span data-stu-id="b1e09-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="b1e09-113">Чтобы получить события мыши или клавиатуры из окна видео, приложение должно задать *сток сообщений*, в результате чего окно видео пересылает эти сообщения приложению.</span><span class="sxs-lookup"><span data-stu-id="b1e09-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="b1e09-114">Чтобы избежать проблем с обрезкой, в окне видео должны быть установлены нужные стили окна.</span><span class="sxs-lookup"><span data-stu-id="b1e09-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="b1e09-115">Безоконный режим позволяет избежать этих проблем, нарисуйте VMR непосредственно в клиентской области окна приложения, используя DirectDraw для обрезки прямоугольника видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="b1e09-116">Режим без окон значительно сокращает вероятность взаимоблокировок.</span><span class="sxs-lookup"><span data-stu-id="b1e09-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="b1e09-117">Кроме того, приложению не нужно задавать окно владельца или стили окна.</span><span class="sxs-lookup"><span data-stu-id="b1e09-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="b1e09-118">Фактически, когда VMR находится в режиме без окон, он даже не предоставляет интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) , который больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="b1e09-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="b1e09-119">Чтобы использовать режим без окон, необходимо явно настроить VMR.</span><span class="sxs-lookup"><span data-stu-id="b1e09-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="b1e09-120">Однако вы обнаружите, что более гибкий и простой в использовании, чем оконный режим.</span><span class="sxs-lookup"><span data-stu-id="b1e09-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="b1e09-121">Фильтр VMR-7 и фильтр VMR-9 предоставляют различные интерфейсы, но эти шаги эквивалентны для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="b1e09-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="b1e09-122">Настройка VMR для режима без окон</span><span class="sxs-lookup"><span data-stu-id="b1e09-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="b1e09-123">Чтобы переопределить поведение VMR по умолчанию, настройте VMR перед построением графа фильтра:</span><span class="sxs-lookup"><span data-stu-id="b1e09-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="b1e09-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="b1e09-124">**VMR-7**</span></span>

1.  <span data-ttu-id="b1e09-125">Создайте диспетчер графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="b1e09-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="b1e09-126">Создайте VMR-7 и добавьте его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="b1e09-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="b1e09-127">Вызовите [**ивмрфилтерконфиг:: сетрендерингмоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) в VMR-7 с флагом без **\_ окон вмрмоде** .</span><span class="sxs-lookup"><span data-stu-id="b1e09-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="b1e09-128">Запросите VMR-7 для интерфейса [**ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="b1e09-129">Вызовите [**ивмрвиндовлессконтрол:: сетвидеоклиппингвиндов**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) на VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b1e09-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="b1e09-130">Укажите маркер окна, в котором должно появиться видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="b1e09-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="b1e09-131">**VMR-9**</span></span>

1.  <span data-ttu-id="b1e09-132">Создайте диспетчер графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="b1e09-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="b1e09-133">Создайте VMR-9 и добавьте его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="b1e09-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="b1e09-134">Вызовите [**IVMRFilterConfig9:: сетрендерингмоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) в VMR-9 с флагом без **\_ окон VMR9Mode** .</span><span class="sxs-lookup"><span data-stu-id="b1e09-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="b1e09-135">Запросите VMR-9 для интерфейса [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="b1e09-136">Вызовите [**IVMRWindowlessControl9:: сетвидеоклиппингвиндов**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) в VMR-9.</span><span class="sxs-lookup"><span data-stu-id="b1e09-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="b1e09-137">Укажите маркер окна, в котором должно появиться видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="b1e09-138">Теперь создайте остальную часть графа фильтра, вызвав [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) или другие методы построения графа.</span><span class="sxs-lookup"><span data-stu-id="b1e09-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="b1e09-139">Диспетчер графов фильтров автоматически использует экземпляр VMR, добавленный в граф.</span><span class="sxs-lookup"><span data-stu-id="b1e09-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="b1e09-140">(Дополнительные сведения о том, почему это происходит, см. в разделе [Intelligent Connect](intelligent-connect.md).)</span><span class="sxs-lookup"><span data-stu-id="b1e09-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="b1e09-141">В следующем коде показана вспомогательная функция, которая создает VMR-7, добавляет его в граф и настраивает режим без окон.</span><span class="sxs-lookup"><span data-stu-id="b1e09-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="b1e09-142">Эта функция предполагает, что отображает только один видеопоток и не смешивает статический точечный рисунок по видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="b1e09-143">Дополнительные сведения см. в разделе [режим без окон VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="b1e09-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="b1e09-144">Эту функцию следует вызывать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b1e09-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="b1e09-145">Размещение видео</span><span class="sxs-lookup"><span data-stu-id="b1e09-145">Position the Video</span></span>

<span data-ttu-id="b1e09-146">Следующим шагом после настройки VMR является установка расположения видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="b1e09-147">Есть два прямоугольника, которые следует учитывать: *Исходный* прямоугольник и *конечный* прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="b1e09-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="b1e09-148">Исходный прямоугольник определяет, какая часть видео будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="b1e09-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="b1e09-149">Прямоугольник назначения определяет область в клиентской области окна, которая будет содержать видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="b1e09-150">VMR обрезает видеоизображение в исходном прямоугольнике и растягивает обрезанное изображение в соответствии с прямоугольником назначения.</span><span class="sxs-lookup"><span data-stu-id="b1e09-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="b1e09-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="b1e09-151">**VMR-7**</span></span>

1.  <span data-ttu-id="b1e09-152">Вызовите метод [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) , чтобы указать оба прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b1e09-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="b1e09-153">Исходный прямоугольник должен быть равен или меньше размера собственного видео. для получения собственного размера видео можно использовать метод [**ивмрвиндовлессконтрол:: жетнативевидеосизе**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="b1e09-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="b1e09-154">**VMR-9**</span></span>

1.  <span data-ttu-id="b1e09-155">Вызовите метод [**IVMRWindowlessControl9:: сетвидеопоситион**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) , чтобы указать оба прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b1e09-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="b1e09-156">Исходный прямоугольник должен быть равен или меньше размера собственного видео. для получения собственного размера видео можно использовать метод [**IVMRWindowlessControl9:: жетнативевидеосизе**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="b1e09-157">Например, следующий код задает исходные и конечные прямоугольники для VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b1e09-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="b1e09-158">Он задает исходный прямоугольник, равный всему видеоизображению, и конечный прямоугольник равен всей клиентской области окна:</span><span class="sxs-lookup"><span data-stu-id="b1e09-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="b1e09-159">Если вы хотите, чтобы видео занимало меньше части клиентской области, измените параметр *ркдест* .</span><span class="sxs-lookup"><span data-stu-id="b1e09-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="b1e09-160">Если вы хотите обрезать изображение видео, измените параметр *рксрк* .</span><span class="sxs-lookup"><span data-stu-id="b1e09-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="b1e09-161">Обработку сообщений окна</span><span class="sxs-lookup"><span data-stu-id="b1e09-161">Handle Window Messages</span></span>

<span data-ttu-id="b1e09-162">Так как VMR не имеет собственного окна, он должен получать уведомления, если требуется перерисовка или изменение размера видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="b1e09-163">Ответьте на следующие сообщения окна, вызвав перечисленные методы VMR.</span><span class="sxs-lookup"><span data-stu-id="b1e09-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="b1e09-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="b1e09-164">**VMR-7**</span></span>

1.  <span data-ttu-id="b1e09-165">[**WM \_ ЗАЛИВка**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="b1e09-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="b1e09-166">Вызовите [**ивмрвиндовлессконтрол:: репаинтвидео**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="b1e09-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="b1e09-167">Этот метод заставляет VMR-7 перекрасить последнюю видеокадр.</span><span class="sxs-lookup"><span data-stu-id="b1e09-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="b1e09-168">[**WM \_ ДИСПЛАЙЧАНЖЕ**](../gdi/wm-displaychange.md): вызов [**ивмрвиндовлессконтрол::D исплаймодечанжед**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="b1e09-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="b1e09-169">Этот метод уведомляет VMR-7 о том, что видео должно отображаться с новым разрешением или глубиной цвета.</span><span class="sxs-lookup"><span data-stu-id="b1e09-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="b1e09-170">[**WM \_ SIZE**](../winmsg/wm-size.md) или [**WM \_ виндовпосчанжед**](../winmsg/wm-windowposchanged.md): повторно Вычислите расположение видео и вызовите [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) , чтобы обновить расположение при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b1e09-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="b1e09-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="b1e09-171">**VMR-9**</span></span>

1.  <span data-ttu-id="b1e09-172">[**WM \_ ЗАЛИВка**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="b1e09-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="b1e09-173">Вызовите [**IVMRWindowlessControl9:: репаинтвидео**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="b1e09-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="b1e09-174">Этот метод заставляет VMR-9 перекрасить последнюю видеокадр.</span><span class="sxs-lookup"><span data-stu-id="b1e09-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="b1e09-175">[**WM \_ ДИСПЛАЙЧАНЖЕ**](../gdi/wm-displaychange.md): вызов [**IVMRWindowlessControl9::D исплаймодечанжед**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="b1e09-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="b1e09-176">Этот метод уведомляет VMR-9 о том, что видео должно отображаться с новым разрешением или глубиной цвета.</span><span class="sxs-lookup"><span data-stu-id="b1e09-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="b1e09-177">[**WM \_ SIZE**](../winmsg/wm-size.md) или [**WM \_ виндовпосчанжед**](../winmsg/wm-windowposchanged.md): повторно Вычислите расположение видео и вызовите [**IVMRWindowlessControl9:: сетвидеопоситион**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) , чтобы обновить расположение при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b1e09-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="b1e09-178">Обработчик по умолчанию для сообщения [**WM \_ виндовпосчанжед**](../winmsg/wm-windowposchanged.md) отправляет сообщение [**о \_ размере WM**](../winmsg/wm-size.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="b1e09-179">Но если приложение перехватывает **WM \_ виндовпосчанжед** и не передает его в [**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), следует вызвать **сетвидеопоситион** в обработчике **WM \_ виндовпосчанжед** в дополнение к обработчику **\_ размера WM** .</span><span class="sxs-lookup"><span data-stu-id="b1e09-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="b1e09-180">В следующем примере показан обработчик сообщений [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e09-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="b1e09-181">Он закрашивает область, определяемую клиентским прямоугольником, за вычетом прямоугольника видео.</span><span class="sxs-lookup"><span data-stu-id="b1e09-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="b1e09-182">Не Нарисуйте на видеопрямоугольнике, так как VMR перерисовывает его, что приведет к мерцанию.</span><span class="sxs-lookup"><span data-stu-id="b1e09-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="b1e09-183">По той же причине не следует задавать кисть фона в классе окна.</span><span class="sxs-lookup"><span data-stu-id="b1e09-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="b1e09-184">Несмотря на то, что необходимо реагировать на сообщения [**WM \_ Paint**](../gdi/wm-paint.md) , для обновления видео ничего не нужно делать между сообщениями **WM \_ Paint** .</span><span class="sxs-lookup"><span data-stu-id="b1e09-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="b1e09-185">Как показано в этом примере, режим без окон позволяет обрабатывать видеоизображение просто как область саморисования в окне.</span><span class="sxs-lookup"><span data-stu-id="b1e09-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1e09-186">См. также</span><span class="sxs-lookup"><span data-stu-id="b1e09-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1e09-187">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="b1e09-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="b1e09-188">Рендеринг видео</span><span class="sxs-lookup"><span data-stu-id="b1e09-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
