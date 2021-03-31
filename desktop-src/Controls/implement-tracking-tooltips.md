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
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="df06e-104">Реализация подсказок отслеживания</span><span class="sxs-lookup"><span data-stu-id="df06e-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="df06e-105">Отслеживание всплывающих подсказок остается видимым, пока приложение не закроет их явным образом, и может динамически изменять расположение на экране.</span><span class="sxs-lookup"><span data-stu-id="df06e-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="df06e-106">Они поддерживаются в [версии 4,70](common-control-versions.md) и более поздних стандартных элементах управления.</span><span class="sxs-lookup"><span data-stu-id="df06e-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="df06e-107">Чтобы создать подсказку для отслеживания, включите \_ флаг TTF Track в элемент **Уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) при отправке сообщения [**ТТМ \_ аддтул**](ttm-addtool.md) .</span><span class="sxs-lookup"><span data-stu-id="df06e-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="df06e-108">Приложение должно вручную активировать (Показать) и деактивировать (скрыть) подсказку отслеживания, отправив сообщение [**ТТМ \_ траккактивате**](ttm-trackactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="df06e-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="df06e-109">Пока активна подсказка для отслеживания, приложение должно указать расположение подсказки, отправив сообщения [**ТТМ \_ траккпоситион**](ttm-trackposition.md) в элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="df06e-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="df06e-110">Так как приложение обрабатывает такие задачи, как размещение подсказки, в подсказках отслеживания не используется **флаг \_ TTF** или сообщение [**ТТМ \_ релайевент**](ttm-relayevent.md) .</span><span class="sxs-lookup"><span data-stu-id="df06e-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="df06e-111">Сообщение [**ТТМ \_ траккпоситион**](ttm-trackposition.md) приводит к тому, что элемент управления ToolTip отображает окно с помощью одного из двух стилей размещения:</span><span class="sxs-lookup"><span data-stu-id="df06e-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="df06e-112">По умолчанию подсказка отображается рядом с соответствующим инструментом в положении, выбранном элементом управления.</span><span class="sxs-lookup"><span data-stu-id="df06e-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="df06e-113">Выбранное расположение относится к координатам, которые вы указали с помощью этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="df06e-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="df06e-114">Если включить **\_ абсолютное значение TTF** в элемент структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , подсказка отобразится в расположении пикселей, указанном в сообщении.</span><span class="sxs-lookup"><span data-stu-id="df06e-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="df06e-115">В этом случае элемент управления не пытается изменить расположение окна подсказки из предоставленных координат.</span><span class="sxs-lookup"><span data-stu-id="df06e-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="df06e-116">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="df06e-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="df06e-117">Технологии</span><span class="sxs-lookup"><span data-stu-id="df06e-117">Technologies</span></span>

-   [<span data-ttu-id="df06e-118">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="df06e-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="df06e-119">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="df06e-119">Prerequisites</span></span>

-   <span data-ttu-id="df06e-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="df06e-120">C/C++</span></span>
-   <span data-ttu-id="df06e-121">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="df06e-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="df06e-122">Инструкции</span><span class="sxs-lookup"><span data-stu-id="df06e-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="df06e-123">Реализация In-Place подсказок</span><span class="sxs-lookup"><span data-stu-id="df06e-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="df06e-124">Элемент **уфлагс** структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , используемой в этом примере, включает флаг " **TTF \_ Absolute** ".</span><span class="sxs-lookup"><span data-stu-id="df06e-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="df06e-125">Без этого флага элемент управления ToolTip выбирает, где отображать подсказку, и ее расположение относительно диалогового окна может неожиданно измениться по мере перемещения указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="df06e-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="df06e-126">`g_toolItem` является глобальной структурой [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="df06e-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="df06e-127">В следующем примере показано, как создать элемент управления ToolTip для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="df06e-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="df06e-128">В примере в качестве средства указывается вся клиентская область главного окна.</span><span class="sxs-lookup"><span data-stu-id="df06e-128">The example specifies the main window's entire client area as the tool.</span></span>


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



### <a name="window-procedure-implementation"></a><span data-ttu-id="df06e-129">Реализация оконной процедуры</span><span class="sxs-lookup"><span data-stu-id="df06e-129">Window Procedure Implementation</span></span>

<span data-ttu-id="df06e-130">Когда указатель мыши находится внутри области клиента, подсказка активна и отображает координаты курсора, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="df06e-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![снимок экрана: диалоговое окно; подсказка показывает координаты x и y указателя мыши](images/tt-tracking.png)

<span data-ttu-id="df06e-132">Следующий пример кода является процедурой окна для диалогового окна, в котором отображается подсказка отслеживания, созданная в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="df06e-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="df06e-133">Глобальная логическая переменная *g \_ траккингмаусе* используется для определения необходимости повторной активации подсказки и сброса отслеживания мыши, чтобы приложение получало уведомления, когда указатель мыши покидает клиентскую область диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="df06e-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="df06e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="df06e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df06e-135">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="df06e-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




