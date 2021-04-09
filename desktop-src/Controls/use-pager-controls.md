---
title: Использование элементов управления страничного навигатора
description: В этом разделе описывается реализация элемента управления страничного навигатора в приложении.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070704"
---
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="43fb7-103">Использование элементов управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="43fb7-103">How to Use Pager Controls</span></span>

<span data-ttu-id="43fb7-104">В этом разделе описывается реализация элемента управления страничного навигатора в приложении.</span><span class="sxs-lookup"><span data-stu-id="43fb7-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="43fb7-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="43fb7-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="43fb7-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="43fb7-106">Technologies</span></span>

-   [<span data-ttu-id="43fb7-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="43fb7-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="43fb7-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="43fb7-108">Prerequisites</span></span>

-   <span data-ttu-id="43fb7-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="43fb7-109">C/C++</span></span>
-   <span data-ttu-id="43fb7-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="43fb7-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="43fb7-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="43fb7-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="43fb7-112">Инициализация элемента управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="43fb7-112">Initialize a Pager Control</span></span>

<span data-ttu-id="43fb7-113">Чтобы использовать элемент управления страничного навигатора, необходимо вызвать функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) с \_ \_ флагом класса ICC пажескроллер, установленным в элементе **двикк** структуры [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="43fb7-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="43fb7-114">Создание элемента управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="43fb7-114">Create a Pager Control</span></span>

<span data-ttu-id="43fb7-115">Используйте [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или API [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="43fb7-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="43fb7-116">Имя класса для элемента управления — [**WC \_ пажескроллер**](common-control-window-classes.md), которое определено в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="43fb7-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="43fb7-117">Стиль [**ПГС \_ горизонтали**](pager-control-styles.md) используется для создания горизонтального страничного навигатора, а для создания вертикального страничного навигатора используется стиль « [**ПГС \_**](pager-control-styles.md) по вертикали».</span><span class="sxs-lookup"><span data-stu-id="43fb7-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="43fb7-118">Так как это дочерний элемент управления, необходимо также использовать стиль [**\_ дочернего элемента WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="43fb7-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="43fb7-119">После создания элемента управления страничного навигатора, скорее всего, потребуется назначить ему автономное окно.</span><span class="sxs-lookup"><span data-stu-id="43fb7-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="43fb7-120">Если автономное окно является дочерним, необходимо сделать дочернее окно дочерним элементом элемента управления страничного навигатора, чтобы размер и расположение рассчитывались правильно.</span><span class="sxs-lookup"><span data-stu-id="43fb7-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="43fb7-121">Затем вы назначаете это окно элементу управления страничного навигатора с помощью сообщения [**PGM \_ сетчилд**](pgm-setchild.md) .</span><span class="sxs-lookup"><span data-stu-id="43fb7-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="43fb7-122">Имейте в виду, что это сообщение фактически не изменяет родительское окно автономного окна. Он просто присваивает автономное окно.</span><span class="sxs-lookup"><span data-stu-id="43fb7-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="43fb7-123">Если автономное окно является одним из стандартных элементов управления, оно должно иметь стиль [**CCS \_ норесизе**](common-control-styles.md) , чтобы предотвратить попытки элемента управления изменить размер элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="43fb7-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="43fb7-124">Обработка уведомлений элемента управления пейджером</span><span class="sxs-lookup"><span data-stu-id="43fb7-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="43fb7-125">Как минимум, необходимо обработать уведомление [ПГН \_ калксизе](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="43fb7-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="43fb7-126">Если не обработать это уведомление и ввести значение ширины или высоты, то стрелки прокрутки в элементе управления страничного навигатора не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="43fb7-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="43fb7-127">Это связано с тем, что элемент управления страничного навигатора использует ширину или высоту, указанные в \_ уведомлении ПГН калксизе, чтобы определить оптимальный размер автономного окна.</span><span class="sxs-lookup"><span data-stu-id="43fb7-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="43fb7-128">В следующем примере показано, как обработать случай уведомления [ПГН \_ калксизе](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="43fb7-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="43fb7-129">В этом примере автономное окно является элементом управления ToolBar, который содержит неизвестное количество кнопок с неизвестным размером.</span><span class="sxs-lookup"><span data-stu-id="43fb7-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="43fb7-130">В примере показано использование сообщения жетмакссизе размером [**ТБ \_**](tb-getmaxsize.md) для определения размера всех элементов на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="43fb7-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="43fb7-131">Затем в примере ширина всех элементов помещается в элемент **ивидс** структуры [**нмпгкалксизе**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) , которая передается в уведомление.</span><span class="sxs-lookup"><span data-stu-id="43fb7-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a><span data-ttu-id="43fb7-132">См. также</span><span class="sxs-lookup"><span data-stu-id="43fb7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43fb7-133">Использование элементов управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="43fb7-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="43fb7-134">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="43fb7-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 