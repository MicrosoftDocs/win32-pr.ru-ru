---
title: Как управлять кнопками с раскрывающимся списком
description: Кнопка раскрывающегося списка может представлять пользователям список параметров.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74443b0d29b3ab39255d7417fd13677769f6a762ebe176e8301a76029db0c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544960"
---
# <a name="how-to-handle-drop-down-buttons"></a>Как управлять кнопками с раскрывающимся списком

Кнопка раскрывающегося списка может представлять пользователям список параметров. Чтобы создать этот стиль кнопки, укажите стиль [**\_ раскрывающегося списка бтнс**](toolbar-control-and-button-styles.md) (также именуемый [**\_ раскрывающимся списком тбстиле**](toolbar-control-and-button-styles.md) для совместимости с предыдущими версиями стандартных элементов управления). Чтобы отобразить кнопку с раскрывающимся списком, необходимо также задать стиль панели инструментов [**тбстиле \_ ex \_ дравддарровс**](toolbar-extended-styles.md) , отправив сообщение сетекстендедстиле в [**ТБ \_**](tb-setextendedstyle.md) .

На следующем рисунке показана раскрывающийся список "Открыть" с открытым контекстным меню и отображением списка файлов. В этом примере панель инструментов имеет стиль [**тбстиле \_ ex \_ дравддарровс**](toolbar-extended-styles.md) .

![снимок экрана: диалоговое окно с тремя элементами панели инструментов, представленными значками; у одной из них Развернутая стрелка раскрывающегося списка и контекстное меню из трех элементов](images/tb-dropdown.png)

На следующем рисунке показана та же панель инструментов, но без стиля [**тбстиле \_ ex \_ дравддарровс**](toolbar-extended-styles.md) .

![снимок экрана предыдущего диалогового окна, но значок с контекстным меню не содержит стрелку раскрывающегося списка](images/tb-dropdown2.png)

Когда пользователь наводит кнопку на панель инструментов, использующую стиль [**\_ раскрывающегося списка бтнс**](toolbar-control-and-button-styles.md) , элемент управления ToolBar отправляет родительскому окну код уведомления [ТБН \_ DROPDOWN](tbn-dropdown.md) .

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="handle-a-drop-down-button"></a>Обработайте кнопку раскрывающегося списка

В следующем примере кода показано, как приложение может поддерживать кнопку раскрывающегося списка в элементе управления ToolBar.


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




