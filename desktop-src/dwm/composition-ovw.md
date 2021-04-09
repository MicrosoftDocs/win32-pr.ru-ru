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
# <a name="enable-and-control-dwm-composition"></a>Включение и Управление композицией DWM

Интерфейсы API композиции диспетчер окон рабочего стола (DWM) предоставляют несколько функций для настройки и запроса основных сведений, которые используются DWM. Эти API позволяют запрашивать и изменять состояние композиции. Кроме того, можно задать и запросить политику отрисовки для различных атрибутов окна DWM.

## <a name="retrieving-colorization-information"></a>Получение сведений о цветовой оттенок

Цвет неклиентской области окна определяется текущей цветовой темой системы. Значение цвета обеспечивается с помощью интерфейсов API DWM, что позволяет приложению сопоставлять пользовательский интерфейс клиента с темой системы.

Чтобы получить доступ к этому значению цвета и отслеживать изменение цвета, используйте функцию [**двмжетколоризатионколор**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) и сообщение [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .

В этом примере показано, как выполнить обработку сообщения об изменении цвета и получить доступ к новому цвету.

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

## <a name="controlling-non-client-region-rendering"></a>Управление отрисовкой вне области клиента

Два визуальных эффекта, которые позволяет DWM, — прозрачность неклиентской области окна, а также эффекты перехода. Приложению может потребоваться отключить или повторно включить эти эффекты в целях применения стилей или совместимости. Следующие функции используются для управления прозрачностью и поведением эффекта перехода.

- [**двмжетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**двмсетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Для получения текущего состояния отрисовки, не относящегося к клиенту, для окна приложения вызовите [**двмжетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) с параметром *дваттрибуте* , для которого задано значение [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Как видно из документации по [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), при передаче этого флага в **двмжетвиндоваттрибуте** полученное значение атрибута имеет тип **bool**. Различные флаги приводят к тому, что **двмжетвиндоваттрибуте** возвращает значения различных типов. Приведем пример кода.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

В следующем примере показано, как использовать флаг [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) с **двмжетвиндоваттрибуте** для получения прямоугольника расширенных границ рамки окна. Документация для этого флага сообщает нам, что полученное значение атрибута имеет тип **Rect**.

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> При вызове [**двмжетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) с флагами для различных атрибутов следует следовать тому же шаблону программирования, приведенному выше. В статье о перечислении [**двмвиндоваттрибуте**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) в строке для каждого флага указывается тип значения, которое необходимо передать указателю в параметре *пваттрибуте* для **двмжетвиндоваттрибуте**. Параметр *кбаттрибуте* содержит размер этого объекта в байтах.

[**Двмсетвиндоваттрибуте**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) позволяет приложению задать политику отрисовки неклиентской области. Эта функция также определяет, как приложение должно работать с эффектами перехода DWM.

В следующем примере отключается визуализация неклиентской области. Это приводит к отключению всех предыдущих вызовов [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) или [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

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

В дополнение к управлению визуализацией неклиентской области [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) также может управлять эффектами перехода DWM. Поведение перехода можно задать с помощью **двмва \_ TRANSITIONS \_ форцедисаблед** в качестве параметра *дваттрибуте* .

## <a name="messages"></a>Сообщения

Следующие сообщения содержат уведомления о событиях DWM. Эти сообщения можно использовать для наблюдения за изменениями, такими как изменения состояния композиции и изменение темы системных цветов.

- [**WM \_ двмколоризатионколорчанжед**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ двмкомпоситиончанжед**](wm-dwmcompositionchanged.md)
- [**WM \_ двмнкрендерингчанжед**](wm-dwmncrenderingchanged.md)
- [**WM \_ двмвиндовмаксимизедчанже**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a>Отключение композиции DWM (Windows 7 и более ранние версии)

> [!WARNING]
> Сведения в этом разделе относятся только к системам Windows 7 и более ранних версий.

Так как DWM использует графический процессор (GPU) для композиции рабочего стола, приложению может потребоваться отключить DWM для совместимости. Приложения, которые получают полный контроль над рабочим столом, например игры, работающие в полноэкранном режиме, должны определить, включен ли DWM, и если это так, отключите его. Для этого требуются две функции.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**двменаблекомпоситион**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Вызов [**двменаблекомпоситион**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) с *фенабле* , установленным в **DWM \_ EC \_ дисаблекомпоситион** , отключает композицию DWM до тех пор, пока вызывающий процесс не завершит работу или композиция не будет включена повторно путем вызова **двменаблекомпоситион** с *фенабле* Set в **DWM \_ EC \_ енаблекомпоситион**. Композиция DWM автоматически перезапускается сразу же после того, как все приложения, у которых отключена композиция, либо завершают работу, либо имеют ручное повторное включение композиции путем вызова **двменаблекомпоситион**.

> [!NOTE]  
> DWM автоматически отключает композицию, когда приложение пытается нарисовать непосредственно на основной поверхности отображения. Композиция будет отключена, пока не будет освобождена поверхность основного устройства этим приложением.
