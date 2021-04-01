---
title: Как перетащить изображение
description: В этом разделе показано, как перетащить изображение на экране. Перетаскивая функции перемещают изображение плавно, в цвете и без мигания курсора. Можно перетащить как маскированные, так и немаскированные изображения.
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da495ef9ee0895c04a856f456fcda3e3125f2957
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794149"
---
# <a name="how-to-drag-an-image"></a>Как перетащить изображение

В этом разделе показано, как перетащить изображение на экране. Перетаскивая функции перемещают изображение плавно, в цвете и без мигания курсора. Можно перетащить как маскированные, так и немаскированные изображения.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="step-1-begin-the-drag-operation"></a>Шаг 1. Начните операцию перетаскивания.

Чтобы начать операцию перетаскивания, используйте функцию [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .

Определяемая пользователем функция в следующем примере кода C++ предназначена для вызова в ответ на сообщение кнопки мыши, например [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown). Функция определяет, щелкнул ли пользователь в ограничивающем прямоугольнике изображения. Если пользователь щелкнул, функция захватывает ввод мыши, стирает изображение из клиентской области и вычисляет место для активной точки в изображении. Функция задает значение активной точки, совпадающей с активной назначением курсора мыши. Затем функция начинает операцию перетаскивания путем вызова [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a>Шаг 2. Перемещение изображения.

Функция [**\_ драгмове ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) перемещает изображение в новое место.

Определяемая пользователем функция в следующем примере кода C++ предназначена для вызова в ответ на сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Он перетаскивать изображение в новое место.


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a>Шаг 3. Завершите операцию перетаскивания.

Определяемая пользователем функция в следующем примере кода C++ вызывает функцию [**ImageList \_ енддраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) для завершения операции перетаскивания. Затем вызывается функция [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) для разблокировки окна и скрытия изображения перетаскивания, что позволяет обновить окно.


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по спискам изображений](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[О списках изображений](image-lists.md)
</dt> <dt>

[Использование списков изображений](using-image-lists.md)
</dt> </dl>

 

 