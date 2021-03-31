---
title: Реализация подсказок отслеживания
description: Отслеживание всплывающих подсказок остается видимым, пока приложение не закроет их явным образом, и может динамически изменять расположение на экране. Они поддерживаются в версии 4,70 и более поздних стандартных элементах управления.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067544"
---
# <a name="how-to-implement-tracking-tooltips"></a>Реализация подсказок отслеживания

Отслеживание всплывающих подсказок остается видимым, пока приложение не закроет их явным образом, и может динамически изменять расположение на экране. Они поддерживаются в [версии 4,70](common-control-versions.md) и более поздних стандартных элементах управления.

Чтобы создать подсказку для отслеживания, включите \_ флаг TTF Track в элемент **Уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) при отправке сообщения [**ТТМ \_ аддтул**](ttm-addtool.md) .

Приложение должно вручную активировать (Показать) и деактивировать (скрыть) подсказку отслеживания, отправив сообщение [**ТТМ \_ траккактивате**](ttm-trackactivate.md) . Пока активна подсказка для отслеживания, приложение должно указать расположение подсказки, отправив сообщения [**ТТМ \_ траккпоситион**](ttm-trackposition.md) в элемент управления ToolTip. Так как приложение обрабатывает такие задачи, как размещение подсказки, в подсказках отслеживания не используется **флаг \_ TTF** или сообщение [**ТТМ \_ релайевент**](ttm-relayevent.md) .

Сообщение [**ТТМ \_ траккпоситион**](ttm-trackposition.md) приводит к тому, что элемент управления ToolTip отображает окно с помощью одного из двух стилей размещения:

-   По умолчанию подсказка отображается рядом с соответствующим инструментом в положении, выбранном элементом управления. Выбранное расположение относится к координатам, которые вы указали с помощью этого сообщения.
-   Если включить **\_ абсолютное значение TTF** в элемент структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , подсказка отобразится в расположении пикселей, указанном в сообщении. В этом случае элемент управления не пытается изменить расположение окна подсказки из предоставленных координат.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="implement-in-place-tooltips"></a>Реализация In-Place подсказок

Элемент **уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , используемой в этом примере, включает флаг " **TTF \_ Absolute** ". Без этого флага элемент управления ToolTip выбирает, где отображать подсказку, и ее расположение относительно диалогового окна может неожиданно измениться по мере перемещения указателя мыши.

> [!Note]  
> `g_toolItem` является глобальной структурой [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .

 

В следующем примере показано, как создать элемент управления ToolTip для отслеживания. В примере в качестве средства указывается вся клиентская область главного окна.


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a>Реализация оконной процедуры

Когда указатель мыши находится внутри области клиента, подсказка активна и отображает координаты курсора, как показано на следующем рисунке.

![снимок экрана: диалоговое окно; подсказка показывает координаты x и y указателя мыши](images/tt-tracking.png)

Следующий пример кода является процедурой окна для диалогового окна, в котором отображается подсказка отслеживания, созданная в предыдущем примере. Глобальная логическая переменная *g \_ траккингмаусе* используется для определения необходимости повторной активации подсказки и сброса отслеживания мыши, чтобы приложение получало уведомления, когда указатель мыши покидает клиентскую область диалогового окна.


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




