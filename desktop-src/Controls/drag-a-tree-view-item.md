---
title: Перетаскивание элемента Tree-View
description: В этом разделе демонстрируется код для обработки перетаскивания элементов представления в виде дерева.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488401"
---
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="115c3-103">Перетаскивание элемента Tree-View</span><span class="sxs-lookup"><span data-stu-id="115c3-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="115c3-104">В этом разделе демонстрируется код для обработки перетаскивания элементов представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="115c3-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="115c3-105">Пример кода состоит из трех функций.</span><span class="sxs-lookup"><span data-stu-id="115c3-105">The sample code consists of three functions.</span></span> <span data-ttu-id="115c3-106">Первая функция начинает операцию перетаскивания, вторая функция перетаскивает изображение, а третья функция завершает операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="115c3-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="115c3-107">При перетаскивании элемента древовидного представления обычно обрабатывается код уведомления [ТВН \_ бегиндраг](tvn-begindrag.md) (или [ТВН \_ бегинрдраг](tvn-beginrdrag.md)), сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) и сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) (или [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup)).</span><span class="sxs-lookup"><span data-stu-id="115c3-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="115c3-108">Он также включает использование функций со [списками изображений](image-lists.md) для рисования элемента при его перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="115c3-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="115c3-109">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="115c3-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="115c3-110">Технологии</span><span class="sxs-lookup"><span data-stu-id="115c3-110">Technologies</span></span>

-   [<span data-ttu-id="115c3-111">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="115c3-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="115c3-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="115c3-112">Prerequisites</span></span>

-   <span data-ttu-id="115c3-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="115c3-113">C/C++</span></span>
-   <span data-ttu-id="115c3-114">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="115c3-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="115c3-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="115c3-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="115c3-116">Шаг 1. Начало операции перетаскивания в представлении дерева</span><span class="sxs-lookup"><span data-stu-id="115c3-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="115c3-117">Элемент управления представлением в виде дерева отправляет родительскому окну код уведомления [ТВН \_ бегиндраг](tvn-begindrag.md) (или [ТВН \_ бегинрдраг](tvn-beginrdrag.md)) каждый раз, когда пользователь начинает перетаскивать элемент.</span><span class="sxs-lookup"><span data-stu-id="115c3-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="115c3-118">Родительское окно получает уведомление в виде сообщения [**WM \_ Notify**](wm-notify.md) , параметр *lParam* которого является адресом структуры [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="115c3-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="115c3-119">Члены этой структуры включают экранные координаты указателя мыши и структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , содержащую сведения о перетаскиваемый элементе.</span><span class="sxs-lookup"><span data-stu-id="115c3-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="115c3-120">В следующем примере показано, как обрабатывать сообщение [**WM \_ Notify**](wm-notify.md) для получения [ТВН \_ бегиндраг](tvn-begindrag.md).</span><span class="sxs-lookup"><span data-stu-id="115c3-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


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



<span data-ttu-id="115c3-121">Начало операции перетаскивания включает использование функции [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .</span><span class="sxs-lookup"><span data-stu-id="115c3-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="115c3-122">Параметры функции включают в себя маркер для списка изображений, который содержит изображение, используемое во время операции перетаскивания, и индекс изображения.</span><span class="sxs-lookup"><span data-stu-id="115c3-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="115c3-123">Можно предоставить собственный список изображений и изображение, или же можно создать элемент управления "дерево-представление", используя сообщение [**TVM \_ креатедрагимаже**](tvm-createdragimage.md) .</span><span class="sxs-lookup"><span data-stu-id="115c3-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="115c3-124">Поскольку изображение перетаскивания заменяет указатель мыши на длительность операции перетаскивания, [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) требует указать активную точку в изображении.</span><span class="sxs-lookup"><span data-stu-id="115c3-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="115c3-125">Координаты активной точки задаются относительно левого верхнего угла изображения.</span><span class="sxs-lookup"><span data-stu-id="115c3-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="115c3-126">**ImageList \_ Бегиндраг** также требует указать начальное расположение изображения перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="115c3-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="115c3-127">Обычно приложение задает начальное расположение, чтобы активная область изображения перетаскивания соответствовала указателю мыши в момент, когда пользователь начал операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="115c3-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="115c3-128">В следующей функции показано, как начать перетаскивать элемент представления дерева.</span><span class="sxs-lookup"><span data-stu-id="115c3-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="115c3-129">Он использует изображение перетаскивания, предоставляемое элементом управления "дерево-представление", и получает ограничивающий прямоугольник элемента, чтобы определить соответствующую точку для горячей точки.</span><span class="sxs-lookup"><span data-stu-id="115c3-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="115c3-130">Размеры ограничивающего прямоугольника аналогичны размерам изображения.</span><span class="sxs-lookup"><span data-stu-id="115c3-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="115c3-131">Функция захватывает ввод мыши, вызывая отправку сообщений мыши в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="115c3-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="115c3-132">Родительскому окну требуются последующие сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , чтобы определить, куда перетаскивать изображение и сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , чтобы определить, когда нужно завершить операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="115c3-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


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



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="115c3-133">Шаг 2. Перетаскивание элемента представления в виде дерева</span><span class="sxs-lookup"><span data-stu-id="115c3-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="115c3-134">Вы перетаскивайте элемент дерева-представления, вызывая функцию [**ImageList \_ драгмове**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) , когда родительское окно получает сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="115c3-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="115c3-135">В примере также показано, как выполнить проверку попадания во время операции перетаскивания, чтобы определить, следует ли выделять другие элементы в представлении в виде дерева в качестве целевых объектов операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="115c3-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="115c3-136">Шаг 3. завершение операции перетаскивания в представлении дерева</span><span class="sxs-lookup"><span data-stu-id="115c3-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="115c3-137">В следующем примере показано, как завершить операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="115c3-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="115c3-138">Функция [**ImageList \_ енддраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) вызывается, когда родительское окно получает сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="115c3-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="115c3-139">Маркер элемента управления "дерево-представление" передается в функцию.</span><span class="sxs-lookup"><span data-stu-id="115c3-139">The handle of the tree-view control is passed to the function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="115c3-140">См. также</span><span class="sxs-lookup"><span data-stu-id="115c3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="115c3-141">Использование элементов управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="115c3-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="115c3-142">Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="115c3-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 