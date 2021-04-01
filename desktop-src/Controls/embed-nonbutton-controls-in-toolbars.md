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
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>Внедрение элементов управления "некнопки" в панели инструментов

Панели инструментов поддерживают только кнопки; Поэтому, если приложению требуется другой тип управления, необходимо создать дочернее окно. На следующем рисунке показана панель инструментов с внедренным элементом управления "поле ввода".

![снимок экрана: диалоговое окно с элементом управления "поле ввода" на панели инструментов, предшествующий трем значкам панели инструментов](images/tb-withedit.png)

> [!Note]  
> Рассмотрите возможность использования [элементов управления "Главная](rebar-controls.md) панель" вместо размещения элементов управления на панелях инструментов.

 

Любой тип окна можно разместить на панели инструментов. В следующем примере кода элемент управления "поле ввода" добавляется в качестве дочернего элемента для окна элемента управления ToolBar. Так как панель инструментов создана, а затем добавлен элемент управления "поле ввода", необходимо указать пространство для элемента управления "поле ввода". Одним из способов сделать это является добавление разделителя в качестве заполнителя на панели инструментов, установка ширины разделителя в число пикселей, которое требуется зарезервировать.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>Внедрение элемента управления "неbutton" в панель инструментов

В следующем фрагменте кода создается панель инструментов на предыдущем рисунке.


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



Этот пример жестко кодирует размеры дочернего окна; Тем не менее, чтобы сделать приложение более надежным, определите размер панели инструментов и сделайте окно элемента управления редактированием по своему усмотрению.

Может потребоваться, чтобы уведомления элемента управления "поле ввода" переходят в другое окно, например на родительский элемент панели инструментов. Для этого создайте элемент управления "поле ввода" в качестве дочернего элемента родительского окна панели инструментов. Затем измените родительский элемент управления Edit на панель инструментов, как показано ниже.


```
SetParent (hWndEdit, hWndToolbar);
```



Уведомления переходят к исходному родителю. Таким образом, управляющие сообщения отправляются в родительский элемент панели инструментов, даже если окно редактирования находится в окне панели инструментов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




