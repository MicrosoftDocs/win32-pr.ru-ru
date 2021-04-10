---
title: Создание элемента управления Tree-View
description: Чтобы создать элемент управления представления в виде дерева, используйте функцию CreateWindowEx, указав значение WC \_ TREEVIEW для класса Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134666"
---
# <a name="how-to-create-a-tree-view-control"></a>Создание элемента управления Tree-View

Чтобы создать элемент управления представления в виде дерева, используйте функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав значение [**WC \_ TREEVIEW**](common-control-window-classes.md) для класса Window. Класс окна древовидного представления регистрируется в адресном пространстве приложения при загрузке библиотеки DLL общего контроля. Чтобы убедиться, что библиотека DLL загружена, используйте функцию [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="create-an-instance-of-a-tree-view-control"></a>Создание экземпляра элемента управления Tree-View

В следующем примере создается элемент управления представления в виде дерева, размер которого соответствует клиентской области родительского окна. Он также использует определяемые приложением функции для связывания списка изображений с элементом управления и добавления элементов в элемент управления.


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>Комментарии

При создании элемента управления "дерево-представление" можно также отправить ему сообщение [**WM \_ сетфонт**](/windows/desktop/winmsg/wm-setfont) , чтобы задать шрифт, используемый для текста. Перед вставкой элементов необходимо отправить это сообщение. По умолчанию в представлении в виде дерева используется шрифт заголовка значка. Хотя можно настроить шрифт для каждого элемента с помощью [пользовательской прорисовки](custom-draw.md), элемент управления "представление в виде дерева" использует размеры шрифта, указанного в сообщении **WM \_ сетфонт** , для определения расстояния и макета.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления Tree-View](using-treeview.md)
</dt> <dt>

[Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 