---
title: Создание панелей инструментов
description: Чтобы создать панель инструментов, используйте функцию CreateWindowEx, указав класс окна ТУЛБАРКЛАССНАМЕ.
ms.assetid: 5D060291-6ACF-478C-97EC-CD8BD55D1FFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69cd40338eaebc0d9de852519dce34dc9bc8aa4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793962"
---
# <a name="how-to-create-toolbars"></a><span data-ttu-id="8c293-103">Создание панелей инструментов</span><span class="sxs-lookup"><span data-stu-id="8c293-103">How to Create Toolbars</span></span>

<span data-ttu-id="8c293-104">Чтобы создать панель инструментов, используйте функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав класс окна [**тулбаркласснаме**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="8c293-104">To create a toolbar, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**TOOLBARCLASSNAME**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="8c293-105">Результирующая панель инструментов изначально не содержит кнопок.</span><span class="sxs-lookup"><span data-stu-id="8c293-105">The resulting toolbar initially contains no buttons.</span></span> <span data-ttu-id="8c293-106">Добавьте кнопки на панель инструментов с помощью сообщения [**\_ инсертбуттон**](tb-insertbutton.md) [**ТБ \_ аддбуттонс**](tb-addbuttons.md) или ТБ.</span><span class="sxs-lookup"><span data-stu-id="8c293-106">Add buttons to the toolbar by using the [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) message.</span></span> <span data-ttu-id="8c293-107">Необходимо отправить сообщение [**\_ AUTOSIZE**](tb-autosize.md) по размеру ТБ после вставки всех элементов и строк в элемент управления, чтобы заставить панель инструментов повторно вычислить размер в зависимости от содержимого.</span><span class="sxs-lookup"><span data-stu-id="8c293-107">You must send the [**TB\_AUTOSIZE**](tb-autosize.md) message after all the items and strings have been inserted into the control, to cause the toolbar to recalculate its size based on its content.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8c293-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="8c293-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8c293-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="8c293-109">Technologies</span></span>

-   [<span data-ttu-id="8c293-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="8c293-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8c293-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="8c293-111">Prerequisites</span></span>

-   <span data-ttu-id="8c293-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="8c293-112">C/C++</span></span>
-   <span data-ttu-id="8c293-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="8c293-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8c293-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8c293-114">Instructions</span></span>

### <a name="create-a-toolbar"></a><span data-ttu-id="8c293-115">Создание панели инструментов</span><span class="sxs-lookup"><span data-stu-id="8c293-115">Create a Toolbar</span></span>

<span data-ttu-id="8c293-116">В следующем примере кода создается панель инструментов, показанная на рисунке с использованием стандартных системных значков.</span><span class="sxs-lookup"><span data-stu-id="8c293-116">The following example code creates the toolbar shown in the illustration, using standard system icons.</span></span> <span data-ttu-id="8c293-117">Изначально кнопка **сохранить** отключена.</span><span class="sxs-lookup"><span data-stu-id="8c293-117">The **Save** button is initially disabled.</span></span>

![снимок экрана, показывающий диалоговое окно с тремя элементами панели инструментов, расположенными горизонтально, каждый из которых имеет значок и текстовую метку](images/tb-codesample1.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateSimpleToolbar(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0, 
                                      hWndParent, NULL, g_hInst, NULL);
        
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize,   // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, (INT_PTR)L"Save"}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



<span data-ttu-id="8c293-119">В следующем примере одна и та же панель инструментов создается практически так же, но в этом случае строки считываются из ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c293-119">The following example creates the same toolbar in much the same way, but in this case, the strings are read from a resource.</span></span>


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarFromResource(HWND hWndParent)
{
    // Declare and initialize local constants.
    const int ImageListID    = 0;
    const int numButtons     = 3;
    const int bitmapSize     = 16;
    
    const DWORD buttonStyles = BTNS_AUTOSIZE;

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | TBSTYLE_WRAPABLE, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);
    if (hWndToolbar == NULL)
        return NULL;

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    ILC_COLOR16 | ILC_MASK, // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 
                (WPARAM)ImageListID, 
                (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, 
                (WPARAM)IDB_STD_SMALL_COLOR, 
                (LPARAM)HINST_COMMCTRL);

    // Load the text from a resource.
    
    // In the string table, the text for all buttons is a single entry that 
    // appears as "~New~Open~Save~~". The separator character is arbitrary, 
    // but it must appear as the first character of the string. The message 
    // returns the index of the first item, and the items are numbered 
    // consecutively.
    
    int iNew = SendMessage(hWndToolbar, TB_ADDSTRING, 
                           (WPARAM)g_hInst, (LPARAM)IDS_NEW); 
 
    // Initialize button info.
    // IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.
    
    TBBUTTON tbButtons[numButtons] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,  TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN, TBSTATE_ENABLED, buttonStyles, {0}, 0, iNew + 1},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE, 0,               buttonStyles, {0}, 0, iNew + 2}
    };

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Resize the toolbar, and then show it.
    SendMessage(hWndToolbar, TB_AUTOSIZE, 0, 0); 
    ShowWindow(hWndToolbar,  TRUE);
    
    return hWndToolbar;
}
```



## <a name="related-topics"></a><span data-ttu-id="8c293-120">См. также</span><span class="sxs-lookup"><span data-stu-id="8c293-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c293-121">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="8c293-121">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="8c293-122">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="8c293-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 