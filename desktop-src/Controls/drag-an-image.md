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
# <a name="how-to-drag-an-image"></a><span data-ttu-id="de3bd-105">Как перетащить изображение</span><span class="sxs-lookup"><span data-stu-id="de3bd-105">How to Drag an Image</span></span>

<span data-ttu-id="de3bd-106">В этом разделе показано, как перетащить изображение на экране.</span><span class="sxs-lookup"><span data-stu-id="de3bd-106">This topic demonstrates how to drag an image on the screen.</span></span> <span data-ttu-id="de3bd-107">Перетаскивая функции перемещают изображение плавно, в цвете и без мигания курсора.</span><span class="sxs-lookup"><span data-stu-id="de3bd-107">The dragging functions move an image smoothly, in color, and without any flashing of the cursor.</span></span> <span data-ttu-id="de3bd-108">Можно перетащить как маскированные, так и немаскированные изображения.</span><span class="sxs-lookup"><span data-stu-id="de3bd-108">Both masked and unmasked images can be dragged.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="de3bd-109">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="de3bd-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="de3bd-110">Технологии</span><span class="sxs-lookup"><span data-stu-id="de3bd-110">Technologies</span></span>

-   [<span data-ttu-id="de3bd-111">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="de3bd-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="de3bd-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="de3bd-112">Prerequisites</span></span>

-   <span data-ttu-id="de3bd-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="de3bd-113">C/C++</span></span>
-   <span data-ttu-id="de3bd-114">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="de3bd-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="de3bd-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="de3bd-115">Instructions</span></span>

### <a name="step-1-begin-the-drag-operation"></a><span data-ttu-id="de3bd-116">Шаг 1. Начните операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="de3bd-116">Step 1: Begin the drag operation.</span></span>

<span data-ttu-id="de3bd-117">Чтобы начать операцию перетаскивания, используйте функцию [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .</span><span class="sxs-lookup"><span data-stu-id="de3bd-117">Use the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function to begin a drag operation.</span></span>

<span data-ttu-id="de3bd-118">Определяемая пользователем функция в следующем примере кода C++ предназначена для вызова в ответ на сообщение кнопки мыши, например [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="de3bd-118">The user-defined function in the following C++ code example is intended to be called in response to a mouse button-down message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="de3bd-119">Функция определяет, щелкнул ли пользователь в ограничивающем прямоугольнике изображения.</span><span class="sxs-lookup"><span data-stu-id="de3bd-119">The function determines whether the user has clicked within the bounding rectangle of the image.</span></span> <span data-ttu-id="de3bd-120">Если пользователь щелкнул, функция захватывает ввод мыши, стирает изображение из клиентской области и вычисляет место для активной точки в изображении.</span><span class="sxs-lookup"><span data-stu-id="de3bd-120">If the user has clicked, the function captures the mouse input, erases the image from the client area, and calculates the position for the hot spot within the image.</span></span> <span data-ttu-id="de3bd-121">Функция задает значение активной точки, совпадающей с активной назначением курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="de3bd-121">The function sets the hot spot to coincide with the hot spot of the mouse cursor.</span></span> <span data-ttu-id="de3bd-122">Затем функция начинает операцию перетаскивания путем вызова [**ImageList \_ бегиндраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span><span class="sxs-lookup"><span data-stu-id="de3bd-122">Then the function begins the drag operation by calling [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span></span>


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



### <a name="step-2-move-the-image"></a><span data-ttu-id="de3bd-123">Шаг 2. Перемещение изображения.</span><span class="sxs-lookup"><span data-stu-id="de3bd-123">Step 2: Move the image.</span></span>

<span data-ttu-id="de3bd-124">Функция [**\_ драгмове ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) перемещает изображение в новое место.</span><span class="sxs-lookup"><span data-stu-id="de3bd-124">The [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function moves the image to a new location.</span></span>

<span data-ttu-id="de3bd-125">Определяемая пользователем функция в следующем примере кода C++ предназначена для вызова в ответ на сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="de3bd-125">The user-defined function in the following C++ code example is intended to be called in response to the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="de3bd-126">Он перетаскивать изображение в новое место.</span><span class="sxs-lookup"><span data-stu-id="de3bd-126">It drags the image to a new location.</span></span>


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



### <a name="step-3-end-the-drag-operation"></a><span data-ttu-id="de3bd-127">Шаг 3. Завершите операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="de3bd-127">Step 3: End the drag operation.</span></span>

<span data-ttu-id="de3bd-128">Определяемая пользователем функция в следующем примере кода C++ вызывает функцию [**ImageList \_ енддраг**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) для завершения операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="de3bd-128">The user-defined function in the following C++ code example calls the [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function to end the drag operation.</span></span> <span data-ttu-id="de3bd-129">Затем вызывается функция [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) для разблокировки окна и скрытия изображения перетаскивания, что позволяет обновить окно.</span><span class="sxs-lookup"><span data-stu-id="de3bd-129">It then calls the [**ImageList\_DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) function to unlock the window and hide the drag image, allowing the window to be updated.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="de3bd-130">См. также</span><span class="sxs-lookup"><span data-stu-id="de3bd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de3bd-131">Справочник по спискам изображений</span><span class="sxs-lookup"><span data-stu-id="de3bd-131">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="de3bd-132">О списках изображений</span><span class="sxs-lookup"><span data-stu-id="de3bd-132">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="de3bd-133">Использование списков изображений</span><span class="sxs-lookup"><span data-stu-id="de3bd-133">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 