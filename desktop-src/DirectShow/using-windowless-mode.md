---
description: Использование режима без окон
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Использование режима без окон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5189fb52932a328493baec9a79ccd6598a9a0659c198ee3ce3d4d157574a63c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119271254"
---
# <a name="using-windowless-mode"></a>Использование режима без окон

Оба фильтра модуля подготовки [видео](video-mixing-renderer-filter-7.md) (VMR-7) и i [микширования видео с фильтром 9](video-mixing-renderer-filter-9.md) (VMR-9) поддерживают *безоконный режим*, что представляет собой значительное улучшение по сравнению с интерфейсом [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) . В этом разделе описываются различия между режимом без окон и оконным режимом, а также использование режима без окон.

Чтобы сохранить обратную совместимость с существующими приложениями, параметр VMR по умолчанию имеет режим окон. В оконном режиме модуль подготовки отчетов создает собственное окно для отображения видео. Как правило, приложение устанавливает, что окно видео является дочерним по отношению к окну приложения. Наличие отдельного окна видео вызывает некоторые проблемы.

-   Что важнее всего, существует вероятность возникновения взаимоблокировок при отправке сообщений окна между потоками.
-   фильтр Graph Manager должен пересылать определенные окна сообщений, например WM \_ PAINT, в модуль подготовки видео. приложение должно использовать реализацию [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) диспетчера Graph manager (а не модуль подготовки видео), чтобы диспетчер Graph фильтра сохранит правильное внутреннее состояние.
-   Чтобы получить события мыши или клавиатуры из окна видео, приложение должно задать *сток сообщений*, в результате чего окно видео пересылает эти сообщения приложению.
-   Чтобы избежать проблем с обрезкой, в окне видео должны быть установлены нужные стили окна.

Безоконный режим позволяет избежать этих проблем, нарисуйте VMR непосредственно в клиентской области окна приложения, используя DirectDraw для обрезки прямоугольника видео. Режим без окон значительно сокращает вероятность взаимоблокировок. Кроме того, приложению не нужно задавать окно владельца или стили окна. Фактически, когда VMR находится в режиме без окон, он даже не предоставляет интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) , который больше не нужен.

Чтобы использовать режим без окон, необходимо явно настроить VMR. Однако вы обнаружите, что более гибкий и простой в использовании, чем оконный режим.

Фильтр VMR-7 и фильтр VMR-9 предоставляют различные интерфейсы, но эти шаги эквивалентны для каждого из них.

## <a name="configure-the-vmr-for-windowless-mode"></a>Настройка VMR для режима без окон

Чтобы переопределить поведение VMR по умолчанию, настройте VMR перед построением графа фильтра:

**VMR-7**

1.  создайте фильтр Graph Manager.
2.  Создайте VMR-7 и добавьте его в граф фильтра.
3.  Вызовите [**ивмрфилтерконфиг:: сетрендерингмоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) в VMR-7 с флагом без **\_ окон вмрмоде** .
4.  Запросите VMR-7 для интерфейса [**ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
5.  Вызовите [**ивмрвиндовлессконтрол:: сетвидеоклиппингвиндов**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) на VMR-7. Укажите маркер окна, в котором должно появиться видео.

**VMR-9**

1.  создайте фильтр Graph Manager.
2.  Создайте VMR-9 и добавьте его в граф фильтра.
3.  Вызовите [**IVMRFilterConfig9:: сетрендерингмоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) в VMR-9 с флагом без **\_ окон VMR9Mode** .
4.  Запросите VMR-9 для интерфейса [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
5.  Вызовите [**IVMRWindowlessControl9:: сетвидеоклиппингвиндов**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) в VMR-9. Укажите маркер окна, в котором должно появиться видео.

Теперь создайте остальную часть графа фильтра, вызвав [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) или другие методы построения графа. фильтр Graph Manager автоматически использует экземпляр VMR, добавленный в граф. (дополнительные сведения о том, почему это происходит, см. в разделе [интеллектуальные Подключение](intelligent-connect.md).)

В следующем коде показана вспомогательная функция, которая создает VMR-7, добавляет его в граф и настраивает режим без окон.


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



Эта функция предполагает, что отображает только один видеопоток и не смешивает статический точечный рисунок по видео. Дополнительные сведения см. в разделе [режим без окон VMR](vmr-windowless-mode.md). Эту функцию следует вызывать следующим образом:


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



## <a name="position-the-video"></a>Размещение видео

Следующим шагом после настройки VMR является установка расположения видео. Есть два прямоугольника, которые следует учитывать: *Исходный* прямоугольник и *конечный* прямоугольник. Исходный прямоугольник определяет, какая часть видео будет отображаться. Прямоугольник назначения определяет область в клиентской области окна, которая будет содержать видео. VMR обрезает видеоизображение в исходном прямоугольнике и растягивает обрезанное изображение в соответствии с прямоугольником назначения.

**VMR-7**

1.  Вызовите метод [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) , чтобы указать оба прямоугольника.
2.  Исходный прямоугольник должен быть равен или меньше размера собственного видео. для получения собственного размера видео можно использовать метод [**ивмрвиндовлессконтрол:: жетнативевидеосизе**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) .

**VMR-9**

1.  Вызовите метод [**IVMRWindowlessControl9:: сетвидеопоситион**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) , чтобы указать оба прямоугольника.
2.  Исходный прямоугольник должен быть равен или меньше размера собственного видео. для получения собственного размера видео можно использовать метод [**IVMRWindowlessControl9:: жетнативевидеосизе**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) .

Например, следующий код задает исходные и конечные прямоугольники для VMR-7. Он задает исходный прямоугольник, равный всему видеоизображению, и конечный прямоугольник равен всей клиентской области окна:


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



Если вы хотите, чтобы видео занимало меньше части клиентской области, измените параметр *ркдест* . Если вы хотите обрезать изображение видео, измените параметр *рксрк* .

## <a name="handle-window-messages"></a>Обработку сообщений окна

Так как VMR не имеет собственного окна, он должен получать уведомления, если требуется перерисовка или изменение размера видео. Ответьте на следующие сообщения окна, вызвав перечисленные методы VMR.

**VMR-7**

1.  [**WM \_ ЗАЛИВка**](../gdi/wm-paint.md). Вызовите [**ивмрвиндовлессконтрол:: репаинтвидео**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Этот метод заставляет VMR-7 перекрасить последнюю видеокадр.
2.  [**WM \_ ДИСПЛАЙЧАНЖЕ**](../gdi/wm-displaychange.md): вызов [**ивмрвиндовлессконтрол::D исплаймодечанжед**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Этот метод уведомляет VMR-7 о том, что видео должно отображаться с новым разрешением или глубиной цвета.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) или [**WM \_ виндовпосчанжед**](../winmsg/wm-windowposchanged.md): повторно Вычислите расположение видео и вызовите [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) , чтобы обновить расположение при необходимости.

**VMR-9**

1.  [**WM \_ ЗАЛИВка**](../gdi/wm-paint.md). Вызовите [**IVMRWindowlessControl9:: репаинтвидео**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Этот метод заставляет VMR-9 перекрасить последнюю видеокадр.
2.  [**WM \_ ДИСПЛАЙЧАНЖЕ**](../gdi/wm-displaychange.md): вызов [**IVMRWindowlessControl9::D исплаймодечанжед**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged). Этот метод уведомляет VMR-9 о том, что видео должно отображаться с новым разрешением или глубиной цвета.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) или [**WM \_ виндовпосчанжед**](../winmsg/wm-windowposchanged.md): повторно Вычислите расположение видео и вызовите [**IVMRWindowlessControl9:: сетвидеопоситион**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) , чтобы обновить расположение при необходимости.

> [!Note]  
> Обработчик по умолчанию для сообщения [**WM \_ виндовпосчанжед**](../winmsg/wm-windowposchanged.md) отправляет сообщение [**о \_ размере WM**](../winmsg/wm-size.md) . Но если приложение перехватывает **WM \_ виндовпосчанжед** и не передает его в [**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), следует вызвать **сетвидеопоситион** в обработчике **WM \_ виндовпосчанжед** в дополнение к обработчику **\_ размера WM** .

 

В следующем примере показан обработчик сообщений [**WM \_ Paint**](../gdi/wm-paint.md) . Он закрашивает область, определяемую клиентским прямоугольником, за вычетом прямоугольника видео. Не Нарисуйте на видеопрямоугольнике, так как VMR перерисовывает его, что приведет к мерцанию. По той же причине не следует задавать кисть фона в классе окна.


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



Несмотря на то, что необходимо реагировать на сообщения [**WM \_ Paint**](../gdi/wm-paint.md) , для обновления видео ничего не нужно делать между сообщениями **WM \_ Paint** . Как показано в этом примере, режим без окон позволяет обрабатывать видеоизображение просто как область саморисования в окне.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> <dt>

[Рендеринг видео](video-rendering.md)
</dt> </dl>

 

 
