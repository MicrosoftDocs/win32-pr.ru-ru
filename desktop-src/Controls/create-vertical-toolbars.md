---
title: Создание вертикальных панелей инструментов
description: Ключом к созданию вертикальной панели инструментов является включение CCS \_ по вертикали в стиль окна, а также задание \_ стиля переноса тбстате для каждой кнопки.
ms.assetid: C2EAB160-0D8D-4BB9-AD41-D5175FBE81AB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd32609e81196a94f4298197c33a4cc6e21d117
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103987292"
---
# <a name="how-to-create-vertical-toolbars"></a>Создание вертикальных панелей инструментов

Ключом к созданию вертикальной панели инструментов является включение [**CCS по \_ вертикали**](common-control-styles.md) в стиль окна, а также задание стиля [**\_ переноса тбстате**](toolbar-button-states.md) для каждой кнопки.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="create-a-vertical-toolbar"></a>Создание вертикальной панели инструментов

В следующем примере кода создается вертикальная панель инструментов, показанная на следующем рисунке.

![снимок экрана с диалоговым окном с тремя элементами панели инструментов, расположенными вертикально, каждый из которых имеет только значок](images/tb-vertical.png)


```C++
HIMAGELIST g_hImageList = NULL;

HWND CreateVerticalToolbar(HWND hWndParent)
{
    // Define the buttons.
    // IDM_NEW, IDM_0PEN, and IDM_SAVE are application-defined command IDs.
    
    TBBUTTON tbButtons3[numButtons] = 
    {
        {STD_FILENEW,  IDM_NEW,  TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED | TBSTATE_WRAP, BTNS_BUTTON, {0}, 0L, 0}
    };

    // Create the toolbar window.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, NULL, 
                                      WS_CHILD | WS_VISIBLE | CCS_VERT | WS_BORDER, 0, 0, 0, 0,
                                      hWndParent, NULL, g_hInst, NULL);

    // Create the image list.
    g_hImageList = ImageList_Create(24, 24,                   // Dimensions of individual bitmaps.  
                                    ILC_COLOR16 | ILC_MASK,   // Ensures transparent background.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, 0, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_LARGE_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add them to the toolbar.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE,       (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)&tbButtons3);

    return hWndToolbar;
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




