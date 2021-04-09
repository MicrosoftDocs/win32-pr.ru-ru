---
title: Создание элемента управления "заголовок"
description: В этом разделе показано, как создать элемент управления "заголовок" и разместить его в клиентской области родительского окна.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070883"
---
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="f4d47-103">Создание элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="f4d47-103">How to Create a Header Control</span></span>

<span data-ttu-id="f4d47-104">В этом разделе показано, как создать элемент управления "заголовок" и разместить его в клиентской области родительского окна.</span><span class="sxs-lookup"><span data-stu-id="f4d47-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="f4d47-105">Можно создать элемент управления "заголовок" с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) и указать класс [**окна \_ заголовка WC**](common-control-window-classes.md) и соответствующие [стили элемента управления заголовка](header-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4d47-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="f4d47-106">Этот класс окна регистрируется при загрузке библиотеки DLL общих элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f4d47-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="f4d47-107">Чтобы убедиться, что библиотека DLL загружена, используйте функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="f4d47-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f4d47-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="f4d47-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f4d47-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="f4d47-109">Technologies</span></span>

-   [<span data-ttu-id="f4d47-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="f4d47-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f4d47-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f4d47-111">Prerequisites</span></span>

-   <span data-ttu-id="f4d47-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="f4d47-112">C/C++</span></span>
-   <span data-ttu-id="f4d47-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="f4d47-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f4d47-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f4d47-114">Instructions</span></span>


<span data-ttu-id="f4d47-115">В следующем примере кода C++ сначала вызывается функция [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) для загрузки библиотеки DLL общего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f4d47-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="f4d47-116">Затем он вызывает функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="f4d47-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="f4d47-117">Элемент управления изначально скрыт.</span><span class="sxs-lookup"><span data-stu-id="f4d47-117">The control is initially hidden.</span></span> <span data-ttu-id="f4d47-118">Сообщение [**\_ макета HDM**](hdm-layout.md) используется для вычисления размера и расположения элемента управления в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="f4d47-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="f4d47-119">Затем элемент управления перемещается и становится видимым.</span><span class="sxs-lookup"><span data-stu-id="f4d47-119">The control is then repositioned and made visible.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="f4d47-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f4d47-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d47-121">Сведения об элементах управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="f4d47-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="f4d47-122">Справочник по элементу Header</span><span class="sxs-lookup"><span data-stu-id="f4d47-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f4d47-123">Использование элементов управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="f4d47-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 