---
title: Создание элемента управления "заголовок"
description: В этом разделе показано, как создать элемент управления "заголовок" и разместить его в клиентской области родительского окна.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae5bb3ae9c323d30384f5d058a61393bf6425c2a27dfe67faa9cbedd4b3289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063204"
---
# <a name="how-to-create-a-header-control"></a>Создание элемента управления "заголовок"

В этом разделе показано, как создать элемент управления "заголовок" и разместить его в клиентской области родительского окна. Можно создать элемент управления "заголовок" с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) и указать класс [**окна \_ заголовка WC**](common-control-window-classes.md) и соответствующие [стили элемента управления заголовка](header-control-styles.md). Этот класс окна регистрируется при загрузке библиотеки DLL общих элементов управления. Чтобы убедиться, что библиотека DLL загружена, используйте функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


В следующем примере кода C++ сначала вызывается функция [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) для загрузки библиотеки DLL общего элемента управления. Затем он вызывает функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания элемента управления "заголовок". Элемент управления изначально скрыт. Сообщение [**\_ макета HDM**](hdm-layout.md) используется для вычисления размера и расположения элемента управления в родительском окне. Затем элемент управления перемещается и становится видимым.



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об элементах управления "заголовок"](header-controls.md)
</dt> <dt>

[Справочник по элементу Header](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Использование элементов управления "заголовок"](using-header-controls.md)
</dt> </dl>

 

 