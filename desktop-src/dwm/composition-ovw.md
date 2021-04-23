---
title: Включение и Управление композицией DWM
description: Интерфейсы API композиции диспетчер окон рабочего стола (DWM) предоставляют несколько функций для настройки и запроса основных сведений, которые используются DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Диспетчер окон рабочего стола (DWM), композиция
- DWM (диспетчер окон рабочего стола), композиция
- композиции
- Композиция рабочего стола
- раскраска
- Визуализация вне области клиента
- Диспетчер окон рабочего стола (DWM), выделение цветом
- DWM (диспетчер окон рабочего стола), выделение цветом
- Диспетчер окон рабочего стола (DWM), неклиентская область визуализации
- DWM (диспетчер окон рабочего стола), отрисовка вне области клиента
- Диспетчер окон рабочего стола (DWM), Обмен сообщениями
- DWM (диспетчер окон рабочего стола), Обмен сообщениями
- обмен сообщениями
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888996"
---
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="d948f-116">Включение и Управление композицией DWM</span><span class="sxs-lookup"><span data-stu-id="d948f-116">Enable and control DWM composition</span></span>

<span data-ttu-id="d948f-117">Интерфейсы API композиции диспетчер окон рабочего стола (DWM) предоставляют несколько функций для настройки и запроса основных сведений, которые используются DWM.</span><span class="sxs-lookup"><span data-stu-id="d948f-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="d948f-118">Эти API позволяют запрашивать и изменять состояние композиции.</span><span class="sxs-lookup"><span data-stu-id="d948f-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="d948f-119">Кроме того, можно задать и запросить политику отрисовки для различных атрибутов окна DWM.</span><span class="sxs-lookup"><span data-stu-id="d948f-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="d948f-120">Получение сведений о цветовой оттенок</span><span class="sxs-lookup"><span data-stu-id="d948f-120">Retrieving colorization information</span></span>

<span data-ttu-id="d948f-121">Цвет неклиентской области окна определяется текущей цветовой темой системы.</span><span class="sxs-lookup"><span data-stu-id="d948f-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="d948f-122">Значение цвета обеспечивается с помощью интерфейсов API DWM, что позволяет приложению сопоставлять пользовательский интерфейс клиента с темой системы.</span><span class="sxs-lookup"><span data-stu-id="d948f-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="d948f-123">Чтобы получить доступ к этому значению цвета и отслеживать изменение цвета, используйте функцию [**двмжетколоризатионколор**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) и сообщение [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d948f-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="d948f-124">В этом примере показано, как выполнить обработку сообщения об изменении цвета и получить доступ к новому цвету.</span><span class="sxs-lookup"><span data-stu-id="d948f-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="d948f-125">Управление отрисовкой вне области клиента</span><span class="sxs-lookup"><span data-stu-id="d948f-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="d948f-126">Два визуальных эффекта, которые позволяет DWM, — прозрачность неклиентской области окна, а также эффекты перехода.</span><span class="sxs-lookup"><span data-stu-id="d948f-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="d948f-127">Приложению может потребоваться отключить или повторно включить эти эффекты в целях применения стилей или совместимости.</span><span class="sxs-lookup"><span data-stu-id="d948f-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="d948f-128">Следующие функции используются для управления прозрачностью и поведением эффекта перехода.</span><span class="sxs-lookup"><span data-stu-id="d948f-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="d948f-129">**двмжетвиндоваттрибуте**</span><span class="sxs-lookup"><span data-stu-id="d948f-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="d948f-130">**двмсетвиндоваттрибуте**</span><span class="sxs-lookup"><span data-stu-id="d948f-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="d948f-131">Для получения текущего состояния отрисовки, не относящегося к клиенту, для окна приложения вызовите [**двмжетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) с параметром *дваттрибуте* , для которого задано значение [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span><span class="sxs-lookup"><span data-stu-id="d948f-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="d948f-132">Как видно из документации по [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), при передаче этого флага в **двмжетвиндоваттрибуте** полученное значение атрибута имеет тип **bool**.</span><span class="sxs-lookup"><span data-stu-id="d948f-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="d948f-133">Различные флаги приводят к тому, что **двмжетвиндоваттрибуте** возвращает значения различных типов.</span><span class="sxs-lookup"><span data-stu-id="d948f-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="d948f-134">Приведем пример кода.</span><span class="sxs-lookup"><span data-stu-id="d948f-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="d948f-135">В следующем примере показано, как использовать флаг [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) с **двмжетвиндоваттрибуте** для получения прямоугольника расширенных границ рамки окна.</span><span class="sxs-lookup"><span data-stu-id="d948f-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="d948f-136">Документация для этого флага сообщает нам, что полученное значение атрибута имеет тип **Rect**.</span><span class="sxs-lookup"><span data-stu-id="d948f-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="d948f-137">При вызове [**двмжетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) с флагами для различных атрибутов следует следовать тому же шаблону программирования, приведенному выше.</span><span class="sxs-lookup"><span data-stu-id="d948f-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="d948f-138">В статье о перечислении [**двмвиндоваттрибуте**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) в строке для каждого флага указывается тип значения, которое необходимо передать указателю в параметре *пваттрибуте* для **двмжетвиндоваттрибуте**.</span><span class="sxs-lookup"><span data-stu-id="d948f-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="d948f-139">Параметр *кбаттрибуте* содержит размер этого объекта в байтах.</span><span class="sxs-lookup"><span data-stu-id="d948f-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="d948f-140">[**Двмсетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) позволяет приложению задать политику отрисовки неклиентской области.</span><span class="sxs-lookup"><span data-stu-id="d948f-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="d948f-141">Эта функция также определяет, как приложение должно работать с эффектами перехода DWM.</span><span class="sxs-lookup"><span data-stu-id="d948f-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="d948f-142">В следующем примере отключается визуализация неклиентской области.</span><span class="sxs-lookup"><span data-stu-id="d948f-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="d948f-143">Это приводит к отключению всех предыдущих вызовов [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) или [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="d948f-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

<span data-ttu-id="d948f-144">В дополнение к управлению визуализацией неклиентской области [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) также может управлять эффектами перехода DWM.</span><span class="sxs-lookup"><span data-stu-id="d948f-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="d948f-145">Поведение перехода можно задать с помощью **двмва \_ TRANSITIONS \_ форцедисаблед** в качестве параметра *дваттрибуте* .</span><span class="sxs-lookup"><span data-stu-id="d948f-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="d948f-146">Сообщения</span><span class="sxs-lookup"><span data-stu-id="d948f-146">Messages</span></span>

<span data-ttu-id="d948f-147">Следующие сообщения содержат уведомления о событиях DWM.</span><span class="sxs-lookup"><span data-stu-id="d948f-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="d948f-148">Эти сообщения можно использовать для наблюдения за изменениями, такими как изменения состояния композиции и изменение темы системных цветов.</span><span class="sxs-lookup"><span data-stu-id="d948f-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="d948f-149">**WM \_ двмколоризатионколорчанжед**</span><span class="sxs-lookup"><span data-stu-id="d948f-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="d948f-150">**WM \_ двмкомпоситиончанжед**</span><span class="sxs-lookup"><span data-stu-id="d948f-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="d948f-151">**WM \_ двмнкрендерингчанжед**</span><span class="sxs-lookup"><span data-stu-id="d948f-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="d948f-152">**WM \_ двмвиндовмаксимизедчанже**</span><span class="sxs-lookup"><span data-stu-id="d948f-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="d948f-153">Отключение композиции DWM (Windows 7 и более ранние версии)</span><span class="sxs-lookup"><span data-stu-id="d948f-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="d948f-154">Сведения в этом разделе относятся только к системам Windows 7 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="d948f-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="d948f-155">Так как DWM использует графический процессор (GPU) для композиции рабочего стола, приложению может потребоваться отключить DWM для совместимости.</span><span class="sxs-lookup"><span data-stu-id="d948f-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="d948f-156">Приложения, которые получают полный контроль над рабочим столом, например игры, работающие в полноэкранном режиме, должны определить, включен ли DWM, и если это так, отключите его.</span><span class="sxs-lookup"><span data-stu-id="d948f-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="d948f-157">Для этого требуются две функции.</span><span class="sxs-lookup"><span data-stu-id="d948f-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="d948f-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="d948f-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="d948f-159">**двменаблекомпоситион**</span><span class="sxs-lookup"><span data-stu-id="d948f-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="d948f-160">Вызов [**двменаблекомпоситион**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) с *фенабле* , установленным в **DWM \_ EC \_ дисаблекомпоситион** , отключает композицию DWM до тех пор, пока вызывающий процесс не завершит работу или композиция не будет включена повторно путем вызова **двменаблекомпоситион** с *фенабле* Set в **DWM \_ EC \_ енаблекомпоситион**.</span><span class="sxs-lookup"><span data-stu-id="d948f-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="d948f-161">Композиция DWM автоматически перезапускается сразу же после того, как все приложения, у которых отключена композиция, либо завершают работу, либо имеют ручное повторное включение композиции путем вызова **двменаблекомпоситион**.</span><span class="sxs-lookup"><span data-stu-id="d948f-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="d948f-162">DWM автоматически отключает композицию, когда приложение пытается нарисовать непосредственно на основной поверхности отображения.</span><span class="sxs-lookup"><span data-stu-id="d948f-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="d948f-163">Композиция будет отключена, пока не будет освобождена поверхность основного устройства этим приложением.</span><span class="sxs-lookup"><span data-stu-id="d948f-163">Composition will be disabled until the primary device surface is released by that application.</span></span>
