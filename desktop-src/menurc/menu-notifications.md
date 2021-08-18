---
title: Уведомления меню
description: Уведомления меню
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7370da93f430c62618b5d459e40bfa56cb7a9ff9f960f95eb6ce614cc7273e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734260"
---
# <a name="menu-notifications"></a>Уведомления меню

## <a name="in-this-section"></a>В этом разделе

-   [**\_команда WM**](wm-command.md)
-   [**WM \_ CONTEXTMENU**](wm-contextmenu.md)
-   [**WM \_ ентерменулуп**](wm-entermenuloop.md)
-   [**WM \_ екситменулуп**](wm-exitmenuloop.md)
-   [**WM \_ жеттитлебаринфоекс**](wm-gettitlebarinfoex.md)
-   [**WM \_ MENUCOMMAND**](wm-menucommand.md)
-   [**WM \_ менудраг**](wm-menudrag.md)
-   [**WM \_ менужетобжект**](wm-menugetobject.md)
-   [**WM \_ менурбуттонуп**](wm-menurbuttonup.md)
-   [**WM \_ некстмену**](wm-nextmenu.md)
-   [**WM \_ унинитменупопуп**](wm-uninitmenupopup.md)


## <a name="example"></a>Пример

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
пример, взятый из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples) на GitHub.

 




