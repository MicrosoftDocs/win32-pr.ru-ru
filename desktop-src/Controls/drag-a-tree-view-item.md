---
title: Перетаскивание элемента Tree-View
description: В этом разделе демонстрируется код для обработки перетаскивания элементов представления в виде дерева.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ee7cfc9d4fa7a6e73abd042df583ae9175de8583b050ff9621b7d2789e0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413118"
---
# <a name="how-to-drag-a-tree-view-item"></a>Перетаскивание элемента Tree-View

В этом разделе демонстрируется код для обработки перетаскивания элементов представления в виде дерева. Пример кода состоит из трех функций. Первая функция начинает операцию перетаскивания, вторая функция перетаскивает изображение, а третья функция завершает операцию перетаскивания.

> [!Note]  
> При перетаскивании элемента древовидного представления обычно обрабатывается код уведомления [ТВН \_ бегиндраг](tvn-begindrag.md) (или [ТВН \_ бегинрдраг](tvn-beginrdrag.md)), сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) и сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) (или [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup)). Он также включает использование функций со [списками изображений](image-lists.md) для рисования элемента при его перетаскивании.

 

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Шаг 1. Начало операции перетаскивания в представлении дерева

Элемент управления представлением в виде дерева отправляет родительскому окну код уведомления [ТВН \_ бегиндраг](tvn-begindrag.md) (или [ТВН \_ бегинрдраг](tvn-beginrdrag.md)) каждый раз, когда пользователь начинает перетаскивать элемент. Родительское окно получает уведомление в виде сообщения [**WM \_ Notify**](wm-notify.md) , параметр *lParam* которого является адресом структуры [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Члены этой структуры включают экранные координаты указателя мыши и структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , содержащую сведения о перетаскиваемый элементе.

В следующем примере показано, как обрабатывать сообщение [**WM \_ Notify**](wm-notify.md) для получения [ТВН \_ бегиндраг](tvn-begindrag.md).


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



Начало операции перетаскивания включает использование функции [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) . Параметры функции включают в себя маркер для списка изображений, который содержит изображение, используемое во время операции перетаскивания, и индекс изображения. Можно предоставить собственный список изображений и изображение, или же можно создать элемент управления "дерево-представление", используя сообщение [**TVM \_ креатедрагимаже**](tvm-createdragimage.md) .

Поскольку изображение перетаскивания заменяет указатель мыши на длительность операции перетаскивания, [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) требует указать активную точку в изображении. Координаты активной точки задаются относительно левого верхнего угла изображения. **ImageList \_ Бегиндраг** также требует указать начальное расположение изображения перетаскивания. Обычно приложение задает начальное расположение, чтобы активная область изображения перетаскивания соответствовала указателю мыши в момент, когда пользователь начал операцию перетаскивания.

В следующей функции показано, как начать перетаскивать элемент представления дерева. Он использует изображение перетаскивания, предоставляемое элементом управления "дерево-представление", и получает ограничивающий прямоугольник элемента, чтобы определить соответствующую точку для горячей точки. Размеры ограничивающего прямоугольника аналогичны размерам изображения.

Функция захватывает ввод мыши, вызывая отправку сообщений мыши в родительское окно. Родительскому окну требуются последующие сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , чтобы определить, куда перетаскивать изображение и сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , чтобы определить, когда нужно завершить операцию перетаскивания.


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a>Шаг 2. Перетаскивание элемента представления в виде дерева

Вы перетаскивайте элемент дерева-представления, вызывая функцию [**ImageList \_ драгмове**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) , когда родительское окно получает сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , как показано в следующем примере. В примере также показано, как выполнить проверку попадания во время операции перетаскивания, чтобы определить, следует ли выделять другие элементы в представлении в виде дерева в качестве целевых объектов операции перетаскивания.


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Шаг 3. завершение операции перетаскивания в представлении дерева

В следующем примере показано, как завершить операцию перетаскивания. Функция [**ImageList \_ енддраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) вызывается, когда родительское окно получает сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) . Маркер элемента управления "дерево-представление" передается в функцию.


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления Tree-View](using-treeview.md)
</dt> <dt>

[Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 