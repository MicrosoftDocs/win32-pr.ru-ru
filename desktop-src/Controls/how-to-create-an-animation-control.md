---
title: Создание элемента управления "анимация"
description: В этом разделе показано, как создать элемент управления анимации.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067596"
---
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="0707d-103">Создание элемента управления "анимация"</span><span class="sxs-lookup"><span data-stu-id="0707d-103">How to Create an Animation Control</span></span>

<span data-ttu-id="0707d-104">В этом разделе показано, как создать элемент управления анимации.</span><span class="sxs-lookup"><span data-stu-id="0707d-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="0707d-105">В соответствующем примере кода C++ в диалоговом окне создается элемент управления "анимация".</span><span class="sxs-lookup"><span data-stu-id="0707d-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="0707d-106">Он позиционирует элемент управления анимации под заданным элементом управления и устанавливает размеры элемента управления анимации на основе размеров кадра в Audio-Videoном ролике AVI.</span><span class="sxs-lookup"><span data-stu-id="0707d-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0707d-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="0707d-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0707d-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="0707d-108">Technologies</span></span>

-   [<span data-ttu-id="0707d-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="0707d-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0707d-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0707d-110">Prerequisites</span></span>

-   <span data-ttu-id="0707d-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0707d-111">C/C++</span></span>
-   <span data-ttu-id="0707d-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="0707d-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="0707d-113">Файлы AVI</span><span class="sxs-lookup"><span data-stu-id="0707d-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="0707d-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="0707d-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="0707d-115">Шаг 1. Создание экземпляра элемента управления "анимация".</span><span class="sxs-lookup"><span data-stu-id="0707d-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="0707d-116">Используйте макрос [**анимации \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) , чтобы создать экземпляр элемента управления анимации.</span><span class="sxs-lookup"><span data-stu-id="0707d-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="0707d-117">Шаг 2. размещение элемента управления анимации.</span><span class="sxs-lookup"><span data-stu-id="0707d-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="0707d-118">Получение координат экрана указанной кнопки управления.</span><span class="sxs-lookup"><span data-stu-id="0707d-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="0707d-119">Преобразование координат левого нижнего угла в клиентские координаты.</span><span class="sxs-lookup"><span data-stu-id="0707d-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="0707d-120">Размещение элемента управления "анимация" под указанной кнопкой элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0707d-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="0707d-121">Шаг 3. Откройте ролик AVI.</span><span class="sxs-lookup"><span data-stu-id="0707d-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="0707d-122">Вызовите макрос [**анимировать \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) , чтобы открыть ролик AVI и отобразить первый кадр в элементе управления анимации.</span><span class="sxs-lookup"><span data-stu-id="0707d-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="0707d-123">Вызовите функцию **ShowWindow** , чтобы сделать элемент управления анимацией видимым.</span><span class="sxs-lookup"><span data-stu-id="0707d-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="0707d-124">Полный пример</span><span class="sxs-lookup"><span data-stu-id="0707d-124">Complete example</span></span>


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="0707d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0707d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0707d-126">Об элементах управления анимацией</span><span class="sxs-lookup"><span data-stu-id="0707d-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="0707d-127">Справочник по элементу управления анимацией</span><span class="sxs-lookup"><span data-stu-id="0707d-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0707d-128">Использование элементов управления анимацией</span><span class="sxs-lookup"><span data-stu-id="0707d-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="0707d-129">Анимация</span><span class="sxs-lookup"><span data-stu-id="0707d-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




