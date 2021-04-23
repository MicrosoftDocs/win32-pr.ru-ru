---
title: Создание диалогового окна с вкладками
description: В примере в этом разделе показано, как создать диалоговое окно, в котором используются вкладки для предоставления нескольких страниц элементов управления.
ms.assetid: DBF7FBDF-AADC-45CE-833E-F893C1129FC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0b84a8a77d18903ddbdb29687cc2b97b88872b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891140"
---
# <a name="how-to-create-a-tabbed-dialog-box"></a><span data-ttu-id="1bb5f-103">Создание диалогового окна с вкладками</span><span class="sxs-lookup"><span data-stu-id="1bb5f-103">How to Create a Tabbed Dialog Box</span></span>

<span data-ttu-id="1bb5f-104">В примере в этом разделе показано, как создать диалоговое окно, в котором используются вкладки для предоставления нескольких страниц элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-104">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="1bb5f-105">Главное диалоговое окно является модальным диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-105">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="1bb5f-106">Каждая страница элементов управления определяется шаблоном диалогового окна, имеющим стиль [**\_ дочернего элемента WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="1bb5f-106">Each page of controls is defined by a dialog box template that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style.</span></span> <span data-ttu-id="1bb5f-107">Если выбрана вкладка, то для страницы «входящие» создается немодальное диалоговое окно, и диалоговое окно для исходящей страницы уничтожается.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-107">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="1bb5f-108">Во многих случаях можно легко реализовать несколько диалоговых окон с помощью страниц свойств.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-108">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="1bb5f-109">Дополнительные сведения о страницах свойств см. в разделе [сведения о страницах свойств](property-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="1bb5f-109">For more information about property sheets, see [About Property Sheets](property-sheets.md).</span></span>

 

<span data-ttu-id="1bb5f-110">Шаблон для главного диалогового окна просто определяет два элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="1bb5f-110">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="1bb5f-111">При обработке сообщения [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) процедура диалогового окна создает элемент управления «вкладка» и загружает ресурсы шаблона диалогового окна для каждого из дочерних диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-111">When processing the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1bb5f-112">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="1bb5f-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1bb5f-113">Технологии</span><span class="sxs-lookup"><span data-stu-id="1bb5f-113">Technologies</span></span>

-   [<span data-ttu-id="1bb5f-114">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="1bb5f-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1bb5f-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1bb5f-115">Prerequisites</span></span>

-   <span data-ttu-id="1bb5f-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="1bb5f-116">C/C++</span></span>
-   <span data-ttu-id="1bb5f-117">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="1bb5f-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1bb5f-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="1bb5f-118">Instructions</span></span>

### <a name="create-a-tabbed-dialog-box"></a><span data-ttu-id="1bb5f-119">Создание диалогового окна с вкладками</span><span class="sxs-lookup"><span data-stu-id="1bb5f-119">Create a Tabbed Dialog Box</span></span>

<span data-ttu-id="1bb5f-120">Сведения сохраняются в определяемой приложением структуре с именем ДЛГХДР.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-120">The information is saved in an application-defined structure called DLGHDR.</span></span> <span data-ttu-id="1bb5f-121">Указатель на эту структуру связан с окном диалогового окна с помощью функции [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="1bb5f-121">A pointer to this structure is associated with the dialog box window by using the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function.</span></span> <span data-ttu-id="1bb5f-122">Структура определяется в файле заголовка приложения следующим образом.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-122">The structure is defined in the application's header file, as follows.</span></span>


```C++
#define C_PAGES 3 

typedef struct tag_dlghdr { 
    HWND hwndTab;       // tab control 
    HWND hwndDisplay;   // current child dialog box 
    RECT rcDisplay;     // display rectangle for the tab control 
    DLGTEMPLATEEX *apRes[C_PAGES]; 
} DLGHDR; 
```



<span data-ttu-id="1bb5f-123">Следующая функция обрабатывает сообщение [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) для главного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-123">The following function processes the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message for the main dialog box.</span></span> <span data-ttu-id="1bb5f-124">Функция выделяет `DLGHDR` структуру, загружает ресурсы шаблона диалогового окна для дочерних диалоговых окон и создает элемент управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="1bb5f-124">The function allocates the `DLGHDR` structure, loads the dialog box template resources for the child dialog boxes, and creates the tab control.</span></span>

<span data-ttu-id="1bb5f-125">Размер каждого дочернего диалогового окна определяется структурой [**длгтемплатикс**](/windows/desktop/dlgbox/dlgtemplateex) .</span><span class="sxs-lookup"><span data-stu-id="1bb5f-125">The size of each child dialog box is specified by the [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) structure.</span></span> <span data-ttu-id="1bb5f-126">Функция проверяет размер каждого диалогового окна и использует макрос для сообщения [**TCM \_ аджустрект**](tcm-adjustrect.md) для вычисления соответствующего размера для элемента управления Tab.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-126">The function examines the size of each dialog box and uses the macro for the [**TCM\_ADJUSTRECT**](tcm-adjustrect.md) message to calculate an appropriate size for the tab control.</span></span> <span data-ttu-id="1bb5f-127">Затем он изменяет размер диалогового окна и размещает две кнопки соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-127">Then it sizes the dialog box and positions the two buttons accordingly.</span></span> <span data-ttu-id="1bb5f-128">Этот пример отправляет **TCM \_ аджустрект** с помощью макроса [**\_ аджустрект табктрл**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .</span><span class="sxs-lookup"><span data-stu-id="1bb5f-128">This example sends **TCM\_ADJUSTRECT** by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>


```C++
// Handles the WM_INITDIALOG message for a dialog box that contains 
//   a tab control used to select among three child dialog boxes.
// Returns a result code.
// hwndDlg - handle of the dialog box.
// 
HRESULT OnTabbedDialogInit(HWND hwndDlg) 
{ 
    INITCOMMONCONTROLSEX iccex;
    DWORD dwDlgBase = GetDialogBaseUnits();
    int cxMargin = LOWORD(dwDlgBase) / 4; 
    int cyMargin = HIWORD(dwDlgBase) / 8; 

    TCITEM tie; 
    RECT rcTab; 
    HWND hwndButton; 
    RECT rcButton; 
    int i; 

    // Initialize common controls.
    iccex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    iccex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&iccex); 

    // Allocate memory for the DLGHDR structure. Remember to 
    // free this memory before the dialog box is destroyed.
    DLGHDR *pHdr = (DLGHDR *) LocalAlloc(LPTR, sizeof(DLGHDR)); 

    // Save a pointer to the DLGHDR structure in the window
    // data of the dialog box. 
    SetWindowLongPtr(hwndDlg, GWLP_USERDATA, (LONG_PTR) pHdr); 
 
    // Create the tab control. Note that g_hInst is a global 
    // instance handle. 
    pHdr->hwndTab = CreateWindow( 
        WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, 100, 100, 
        hwndDlg, NULL, g_hInst, NULL 
        ); 
    if (pHdr->hwndTab == NULL) 
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }
 
    // Add a tab for each of the three child dialog boxes. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = L"First"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 0, &tie); 
    tie.pszText = L"Second"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 1, &tie); 
    tie.pszText = L"Third"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 2, &tie); 

    // Lock the resources for the three child dialog boxes. 
    pHdr->apRes[0] = DoLockDlgRes(MAKEINTRESOURCE(IDD_FIRSTDLG)); 
    pHdr->apRes[1] = DoLockDlgRes(MAKEINTRESOURCE(IDD_SECONDDLG)); 
    pHdr->apRes[2] = DoLockDlgRes(MAKEINTRESOURCE(IDD_THIRDDLG)); 

    // Determine a bounding rectangle that is large enough to 
    // contain the largest child dialog box. 
    SetRectEmpty(&rcTab); 
    for (i = 0; i < C_PAGES; i++) 
    { 
        if (pHdr->apRes[i]->cx > rcTab.right) 
            rcTab.right = pHdr->apRes[i]->cx; 
        if (pHdr->apRes[i]->cy > rcTab.bottom) 
            rcTab.bottom = pHdr->apRes[i]->cy; 
    }

    // Map the rectangle from dialog box units to pixels.
    MapDialogRect(hwndDlg, &rcTab);
    
    // Calculate how large to make the tab control, so 
    // the display area can accommodate all the child dialog boxes. 
    TabCtrl_AdjustRect(pHdr->hwndTab, TRUE, &rcTab); 
    OffsetRect(&rcTab, cxMargin - rcTab.left, cyMargin - rcTab.top); 
 
    // Calculate the display rectangle. 
    CopyRect(&pHdr->rcDisplay, &rcTab); 
    TabCtrl_AdjustRect(pHdr->hwndTab, FALSE, &pHdr->rcDisplay); 
 
    // Set the size and position of the tab control, buttons, 
    // and dialog box. 
    SetWindowPos(pHdr->hwndTab, NULL, rcTab.left, rcTab.top, 
            rcTab.right - rcTab.left, rcTab.bottom - rcTab.top, 
            SWP_NOZORDER); 
 
    // Move the first button below the tab control. 
    hwndButton = GetDlgItem(hwndDlg, IDB_CLOSE); 
    SetWindowPos(hwndButton, NULL, 
            rcTab.left, rcTab.bottom + cyMargin, 0, 0, 
            SWP_NOSIZE | SWP_NOZORDER); 
 
    // Determine the size of the button. 
    GetWindowRect(hwndButton, &rcButton); 
    rcButton.right -= rcButton.left; 
    rcButton.bottom -= rcButton.top; 
 
    // Move the second button to the right of the first. 
    hwndButton = GetDlgItem(hwndDlg, IDB_TEST); 
    SetWindowPos(hwndButton, NULL, 
        rcTab.left + rcButton.right + cxMargin, 
        rcTab.bottom + cyMargin, 0, 0, 
        SWP_NOSIZE | SWP_NOZORDER); 
 
    // Size the dialog box. 
    SetWindowPos(hwndDlg, NULL, 0, 0, 
        rcTab.right + cyMargin + (2 * GetSystemMetrics(SM_CXDLGFRAME)), 
        rcTab.bottom + rcButton.bottom + (2 * cyMargin)
        + (2 * GetSystemMetrics(SM_CYDLGFRAME)) 
        + GetSystemMetrics(SM_CYCAPTION), 
        SWP_NOMOVE | SWP_NOZORDER); 
 
    // Simulate selection of the first item. 
    OnSelChanged(hwndDlg); 

    return S_OK;
} 

// Loads and locks a dialog box template resource. 
// Returns the address of the locked dialog box template resource. 
// lpszResName - name of the resource. 
//
DLGTEMPLATEEX* DoLockDlgRes(LPCTSTR lpszResName) 
{ 
    HRSRC hrsrc = FindResource(NULL, lpszResName, RT_DIALOG); 

    // Note that g_hInst is the global instance handle
    HGLOBAL hglb = LoadResource(g_hInst, hrsrc);  
    return (DLGTEMPLATEEX *) LockResource(hglb); 
} 
```



<span data-ttu-id="1bb5f-129">Следующая функция обрабатывает код уведомления [ТКН \_ селчанже](tcn-selchange.md) для главного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-129">The following function processes the [TCN\_SELCHANGE](tcn-selchange.md) notification code for the main dialog box.</span></span> <span data-ttu-id="1bb5f-130">Функция уничтожает диалоговое окно для исходящей страницы, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-130">The function destroys the dialog box for the outgoing page, if any.</span></span> <span data-ttu-id="1bb5f-131">Затем используется функция [**креатедиалогиндирект**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) для создания немодального диалогового окна для входящей страницы.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-131">Then it uses the [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) function to create a modeless dialog box for the incoming page.</span></span>


```C++
// Processes the TCN_SELCHANGE notification. 
// hwndDlg - handle to the parent dialog box. 
//
VOID OnSelChanged(HWND hwndDlg) 
{ 
    // Get the dialog header data.
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndDlg, GWLP_USERDATA); 

    // Get the index of the selected tab.
    int iSel = TabCtrl_GetCurSel(pHdr->hwndTab); 
 
    // Destroy the current child dialog box, if any. 
    if (pHdr->hwndDisplay != NULL) 
        DestroyWindow(pHdr->hwndDisplay); 
 
    // Create the new child dialog box. Note that g_hInst is the
    // global instance handle.
    pHdr->hwndDisplay = CreateDialogIndirect(g_hInst, 
        (DLGTEMPLATE *)pHdr->apRes[iSel], hwndDlg, ChildDialogProc); 

    return;
} 
```



<span data-ttu-id="1bb5f-132">Следующая функция обрабатывает сообщение [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) для каждого из дочерних диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-132">The following function processes the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message for each of the child dialog boxes.</span></span> <span data-ttu-id="1bb5f-133">Нельзя указать расположение диалогового окна, созданного с помощью функции [**креатедиалогиндирект**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) .</span><span class="sxs-lookup"><span data-stu-id="1bb5f-133">You cannot specify the position of a dialog box that is created using the [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) function.</span></span> <span data-ttu-id="1bb5f-134">Эта функция использует функцию [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) для размещения дочернего диалогового окна в области экрана элемента управления Tab.</span><span class="sxs-lookup"><span data-stu-id="1bb5f-134">This function uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to position the child dialog within the tab control's display area.</span></span>


```C++
// Positions the child dialog box to occupy the display area of the 
//   tab control. 
// hwndDlg - handle of the dialog box.
//
VOID WINAPI OnChildDialogInit(HWND hwndDlg) 
{ 
    HWND hwndParent = GetParent(hwndDlg);
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndParent, GWLP_USERDATA); 
    SetWindowPos(hwndDlg, NULL, pHdr->rcDisplay.left,
        pHdr->rcDisplay.top,//-2,
        (pHdr->rcDisplay.right - pHdr->rcDisplay.left),
        (pHdr->rcDisplay.bottom - pHdr->rcDisplay.top),
        SWP_SHOWWINDOW);
        
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="1bb5f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1bb5f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bb5f-136">Использование элементов управления "Вкладка"</span><span class="sxs-lookup"><span data-stu-id="1bb5f-136">Using Tab Controls</span></span>](using-tab-controls.md)
</dt> <dt>

<span data-ttu-id="1bb5f-137">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1bb5f-137">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 