---
title: Создание элемента управления List-View
description: В этом разделе показано, как создать элемент управления "представление списка". Чтобы создать элемент управления "представление списка", используйте функцию CreateWindow или CreateWindowEx и укажите \_ класс окна LISTVIEW WC.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488562"
---
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="bd197-104">Создание элемента управления List-View</span><span class="sxs-lookup"><span data-stu-id="bd197-104">How to Create a List-View Control</span></span>

<span data-ttu-id="bd197-105">В этом разделе показано, как создать элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="bd197-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="bd197-106">Чтобы создать элемент управления "представление списка", используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) и укажите класс окна [**\_ LISTVIEW WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="bd197-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="bd197-107">Элемент управления "представление списка" также можно создать как часть шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="bd197-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="bd197-108">В качестве имени класса необходимо указать [**WC \_ LISTVIEW**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="bd197-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="bd197-109">Чтобы использовать элемент управления "список" как часть шаблона диалогового окна, необходимо вызвать [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) или [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) перед созданием экземпляра диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="bd197-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bd197-110">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="bd197-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bd197-111">Технологии</span><span class="sxs-lookup"><span data-stu-id="bd197-111">Technologies</span></span>

-   [<span data-ttu-id="bd197-112">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="bd197-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bd197-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="bd197-113">Prerequisites</span></span>

-   <span data-ttu-id="bd197-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="bd197-114">C/C++</span></span>
-   <span data-ttu-id="bd197-115">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="bd197-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bd197-116">Инструкции</span><span class="sxs-lookup"><span data-stu-id="bd197-116">Instructions</span></span>


<span data-ttu-id="bd197-117">Сначала зарегистрируйте класс окна, вызвав функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) и указав бит [**для \_ \_ классов элементов ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) в сопутствующей структуре **InitCommonControlsEx** .</span><span class="sxs-lookup"><span data-stu-id="bd197-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="bd197-118">Это гарантирует, что библиотека DLL общих элементов управления будет загружена.</span><span class="sxs-lookup"><span data-stu-id="bd197-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="bd197-119">Затем используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) и укажите класс окна [**\_ LISTVIEW WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="bd197-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="bd197-120">По умолчанию элемент управления "представление списка" использует шрифт заголовка значка.</span><span class="sxs-lookup"><span data-stu-id="bd197-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="bd197-121">Однако можно использовать сообщение [**WM \_ сетфонт**](/windows/desktop/winmsg/wm-setfont) , чтобы указать шрифт, используемый для текста.</span><span class="sxs-lookup"><span data-stu-id="bd197-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="bd197-122">Перед вставкой элементов необходимо отправить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="bd197-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="bd197-123">Для определения расстояния и макета элемент управления использует размеры шрифта, заданные в сообщении **WM \_ сетфонт** .</span><span class="sxs-lookup"><span data-stu-id="bd197-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="bd197-124">Можно также настроить шрифт для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="bd197-124">You can also customize the font for each item.</span></span> <span data-ttu-id="bd197-125">Дополнительные сведения см. в разделе [Пользовательская прорисовка](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="bd197-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="bd197-126">В следующем примере кода C++ создается элемент управления "представление списка" в представлении отчетов.</span><span class="sxs-lookup"><span data-stu-id="bd197-126">The following C++ code example creates a list-view control in report view.</span></span>


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




<span data-ttu-id="bd197-127">Как правило, приложения List-View позволяют пользователю перейти с одного представления на другое.</span><span class="sxs-lookup"><span data-stu-id="bd197-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="bd197-128">В следующем примере кода C++ изменяется стиль окна списка, который, в свою очередь, изменяет представление.</span><span class="sxs-lookup"><span data-stu-id="bd197-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="bd197-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bd197-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd197-130">Справочник по элементу управления представления списка</span><span class="sxs-lookup"><span data-stu-id="bd197-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bd197-131">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="bd197-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="bd197-132">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="bd197-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 