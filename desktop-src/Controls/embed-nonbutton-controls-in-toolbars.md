---
title: Внедрение элементов управления "некнопки" в панели инструментов
description: Панели инструментов поддерживают только кнопки; Поэтому, если приложению требуется другой тип управления, необходимо создать дочернее окно. На следующем рисунке показана панель инструментов с внедренным элементом управления "поле ввода".
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103890336"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="9d73b-104">Внедрение элементов управления "некнопки" в панели инструментов</span><span class="sxs-lookup"><span data-stu-id="9d73b-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="9d73b-105">Панели инструментов поддерживают только кнопки; Поэтому, если приложению требуется другой тип управления, необходимо создать дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="9d73b-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="9d73b-106">На следующем рисунке показана панель инструментов с внедренным элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9d73b-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![снимок экрана: диалоговое окно с элементом управления "поле ввода" на панели инструментов, предшествующий трем значкам панели инструментов](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="9d73b-108">Рассмотрите возможность использования [элементов управления "Главная](rebar-controls.md) панель" вместо размещения элементов управления на панелях инструментов.</span><span class="sxs-lookup"><span data-stu-id="9d73b-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="9d73b-109">Любой тип окна можно разместить на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9d73b-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="9d73b-110">В следующем примере кода элемент управления "поле ввода" добавляется в качестве дочернего элемента для окна элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="9d73b-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="9d73b-111">Так как панель инструментов создана, а затем добавлен элемент управления "поле ввода", необходимо указать пространство для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9d73b-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="9d73b-112">Одним из способов сделать это является добавление разделителя в качестве заполнителя на панели инструментов, установка ширины разделителя в число пикселей, которое требуется зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="9d73b-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9d73b-113">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="9d73b-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9d73b-114">Технологии</span><span class="sxs-lookup"><span data-stu-id="9d73b-114">Technologies</span></span>

-   [<span data-ttu-id="9d73b-115">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="9d73b-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9d73b-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="9d73b-116">Prerequisites</span></span>

-   <span data-ttu-id="9d73b-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="9d73b-117">C/C++</span></span>
-   <span data-ttu-id="9d73b-118">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="9d73b-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9d73b-119">Инструкции</span><span class="sxs-lookup"><span data-stu-id="9d73b-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="9d73b-120">Внедрение элемента управления "неbutton" в панель инструментов</span><span class="sxs-lookup"><span data-stu-id="9d73b-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="9d73b-121">В следующем фрагменте кода создается панель инструментов на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9d73b-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="9d73b-122">Этот пример жестко кодирует размеры дочернего окна; Тем не менее, чтобы сделать приложение более надежным, определите размер панели инструментов и сделайте окно элемента управления редактированием по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="9d73b-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="9d73b-123">Может потребоваться, чтобы уведомления элемента управления "поле ввода" переходят в другое окно, например на родительский элемент панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9d73b-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="9d73b-124">Для этого создайте элемент управления "поле ввода" в качестве дочернего элемента родительского окна панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9d73b-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="9d73b-125">Затем измените родительский элемент управления Edit на панель инструментов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9d73b-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="9d73b-126">Уведомления переходят к исходному родителю.</span><span class="sxs-lookup"><span data-stu-id="9d73b-126">Notifications go to the original parent.</span></span> <span data-ttu-id="9d73b-127">Таким образом, управляющие сообщения отправляются в родительский элемент панели инструментов, даже если окно редактирования находится в окне панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9d73b-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d73b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9d73b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d73b-129">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="9d73b-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="9d73b-130">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9d73b-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




