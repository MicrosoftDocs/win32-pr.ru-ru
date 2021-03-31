---
title: Уведомления меню
description: .
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61f5303253fd3201fd9a4510ecf90fa76c10524
ms.sourcegitcommit: e98f40bef170ae9ce30d91ba96b90600b0446a24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/28/2020
ms.locfileid: "104336729"
---
# <a name="menu-notifications"></a>Уведомления меню

## <a name="in-this-section"></a>в этом разделе

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
Пример, взятый из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples) на сайте GitHub.

 




