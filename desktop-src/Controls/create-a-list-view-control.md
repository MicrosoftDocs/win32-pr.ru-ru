---
title: Создание элемента управления List-View
description: В этом разделе показано, как создать элемент управления "представление списка". Чтобы создать элемент управления "представление списка", используйте функцию CreateWindow или CreateWindowEx и укажите \_ класс окна LISTVIEW WC.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826614"
---
# <a name="how-to-create-a-list-view-control"></a>Создание элемента управления List-View

В этом разделе показано, как создать элемент управления "представление списка". Чтобы создать элемент управления "представление списка", используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) и укажите класс окна [**\_ LISTVIEW WC**](common-control-window-classes.md) .

Элемент управления "представление списка" также можно создать как часть шаблона диалогового окна. В качестве имени класса необходимо указать [**WC \_ LISTVIEW**](common-control-window-classes.md) . Чтобы использовать элемент управления "список" как часть шаблона диалогового окна, необходимо вызвать [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) или [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) перед созданием экземпляра диалогового окна.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Сначала зарегистрируйте класс окна, вызвав функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) и указав бит [**для \_ \_ классов элементов ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) в сопутствующей структуре **InitCommonControlsEx** . Это гарантирует, что библиотека DLL общих элементов управления будет загружена. Затем используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) и укажите класс окна [**\_ LISTVIEW WC**](common-control-window-classes.md) .

> [!Note]  
> По умолчанию элемент управления "представление списка" использует шрифт заголовка значка. Однако можно использовать сообщение [**WM \_ сетфонт**](/windows/desktop/winmsg/wm-setfont) , чтобы указать шрифт, используемый для текста. Перед вставкой элементов необходимо отправить это сообщение. Для определения расстояния и макета элемент управления использует размеры шрифта, заданные в сообщении **WM \_ сетфонт** . Можно также настроить шрифт для каждого элемента. Дополнительные сведения см. в разделе [Пользовательская прорисовка](custom-draw.md).

 

В следующем примере кода C++ создается элемент управления "представление списка" в представлении отчетов.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




Как правило, приложения List-View позволяют пользователю перейти с одного представления на другое.

В следующем примере кода C++ изменяется стиль окна списка, который, в свою очередь, изменяет представление.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по элементу управления представления списка](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Сведения об элементах управления List-View](list-view-controls-overview.md)
</dt> <dt>

[Использование элементов управления List-View](using-list-view-controls.md)
</dt> </dl>

 

 