---
title: Создание элементов управления "Главная панель"
description: Приложение создает элемент управления главной панели путем вызова функции CreateWindowEx, указывая РЕБАРКЛАССНАМЕ в качестве класса Window.
ms.assetid: F17CC2A4-BDC6-48A6-9AF5-19FCF65CC39A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b38cd49e8e6016dafad5ec07c77be570a5a430
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793981"
---
# <a name="how-to-create-rebar-controls"></a><span data-ttu-id="0a67a-103">Создание элементов управления "Главная панель"</span><span class="sxs-lookup"><span data-stu-id="0a67a-103">How to Create Rebar Controls</span></span>

<span data-ttu-id="0a67a-104">Приложение создает элемент управления главной панели путем вызова функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указывая [**ребаркласснаме**](common-control-window-classes.md) в качестве класса Window.</span><span class="sxs-lookup"><span data-stu-id="0a67a-104">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="0a67a-105">Приложение должно сначала зарегистрировать класс окна, вызвав функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , указав \_ бит замечательных классов ICC \_ в сопровождающей структуре [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="0a67a-105">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0a67a-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="0a67a-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0a67a-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="0a67a-107">Technologies</span></span>

-   [<span data-ttu-id="0a67a-108">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="0a67a-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0a67a-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0a67a-109">Prerequisites</span></span>

-   <span data-ttu-id="0a67a-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="0a67a-110">C/C++</span></span>
-   <span data-ttu-id="0a67a-111">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="0a67a-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0a67a-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="0a67a-112">Instructions</span></span>

### <a name="create-a-rebar-control"></a><span data-ttu-id="0a67a-113">Создание элемента управления "Главная панель"</span><span class="sxs-lookup"><span data-stu-id="0a67a-113">Create a Rebar Control</span></span>

<span data-ttu-id="0a67a-114">В следующем примере создается элемент управления "Главная панель" с двумя полосами: одна содержит поле со списком и другое, содержащее панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="0a67a-114">The following example creates a rebar control with two bands—one that contains a combo box, and another one that contains a toolbar.</span></span> <span data-ttu-id="0a67a-115">(См. рисунок в разделе [Общие сведения об элементах управления главной панели](rebar-controls.md).) Эти элементы управления создаются отдельно и передаются в пример функции в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="0a67a-115">(See the illustration in [About Rebar Controls](rebar-controls.md).) These controls are created separately, and are passed to the example function as parameters.</span></span>


```C++
#define NUMBUTTONS 3

HWND CreateRebar(HWND hwndOwner, HWND hwndToolbar, HWND hwndCombo)
{
    // Check parameters.
    if ((hwndToolbar == NULL) || (hwndCombo == NULL))
    {
        return NULL;
    }

    // Initialize common controls.
    INITCOMMONCONTROLSEX icex;
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC   = ICC_COOL_CLASSES | ICC_BAR_CLASSES;
    InitCommonControlsEx(&icex);

    // Create the rebar.
    HWND hwndRebar = CreateWindowEx(WS_EX_TOOLWINDOW,
        REBARCLASSNAME,
        NULL,
        WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |
        WS_CLIPCHILDREN | RBS_VARHEIGHT |
        CCS_NODIVIDER | RBS_BANDBORDERS,
        0,0,0,0,
        hwndOwner,
        NULL,
        g_hInst, // global instance handle
        NULL);

    if(!hwndRebar)
    {
        return NULL;
    }

    // Initialize band info used by both bands.
    REBARBANDINFO rbBand = { sizeof(REBARBANDINFO) };
    rbBand.fMask  = 
          RBBIM_STYLE       // fStyle is valid.
        | RBBIM_TEXT        // lpText is valid.
        | RBBIM_CHILD       // hwndChild is valid.
        | RBBIM_CHILDSIZE   // child size members are valid.
        | RBBIM_SIZE;       // cx is valid
    rbBand.fStyle = RBBS_CHILDEDGE | RBBS_GRIPPERALWAYS;  

    // Get the height of the toolbar.
    DWORD dwBtnSize = (DWORD)SendMessage(hwndToolbar, TB_GETBUTTONSIZE, 0,0);

    // Set values unique to the band with the toolbar.
    rbBand.lpText = TEXT("");
    rbBand.hwndChild = hwndToolbar;
    rbBand.cyChild = LOWORD(dwBtnSize);
    rbBand.cxMinChild = NUMBUTTONS * HIWORD(dwBtnSize);
    rbBand.cyMinChild = LOWORD(dwBtnSize);
    // The default width is the width of the buttons.
    rbBand.cx = 0;

    // Add the band that has the toolbar.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);

    // Set values unique to the band with the combo box.
    RECT rc;
    GetWindowRect(hwndCombo, &rc);
    rbBand.lpText = TEXT("Font");
    rbBand.hwndChild = hwndCombo;
    rbBand.cxMinChild = 0;
    rbBand.cyMinChild = rc.bottom - rc.top;
    // The default width should be set to some value wider than the text. The combo 
    // box itself will expand to fill the band.
    rbBand.cx = 100;

    // Add the band that has the combo box.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);
    
    return (hwndRebar);
}
```



## <a name="related-topics"></a><span data-ttu-id="0a67a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="0a67a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a67a-117">Использование элементов управления "Главная панель"</span><span class="sxs-lookup"><span data-stu-id="0a67a-117">Using Rebar Controls</span></span>](using-rebar-controls.md)
</dt> <dt>

[<span data-ttu-id="0a67a-118">Общие сведения об элементах управления главной панели</span><span class="sxs-lookup"><span data-stu-id="0a67a-118">About Rebar Controls</span></span>](rebar-controls.md)
</dt> <dt>

<span data-ttu-id="0a67a-119">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0a67a-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 