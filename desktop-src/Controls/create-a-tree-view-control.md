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
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="ccfd3-103">Создание элемента управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="ccfd3-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="ccfd3-104">Чтобы создать элемент управления представления в виде дерева, используйте функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав значение [**WC \_ TREEVIEW**](common-control-window-classes.md) для класса Window.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="ccfd3-105">Класс окна древовидного представления регистрируется в адресном пространстве приложения при загрузке библиотеки DLL общего контроля.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="ccfd3-106">Чтобы убедиться, что библиотека DLL загружена, используйте функцию [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="ccfd3-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ccfd3-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="ccfd3-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ccfd3-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="ccfd3-108">Technologies</span></span>

-   [<span data-ttu-id="ccfd3-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="ccfd3-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ccfd3-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ccfd3-110">Prerequisites</span></span>

-   <span data-ttu-id="ccfd3-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ccfd3-111">C/C++</span></span>
-   <span data-ttu-id="ccfd3-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="ccfd3-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ccfd3-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="ccfd3-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="ccfd3-114">Создание экземпляра элемента управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="ccfd3-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="ccfd3-115">В следующем примере создается элемент управления представления в виде дерева, размер которого соответствует клиентской области родительского окна.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="ccfd3-116">Он также использует определяемые приложением функции для связывания списка изображений с элементом управления и добавления элементов в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="ccfd3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccfd3-117">Remarks</span></span>

<span data-ttu-id="ccfd3-118">При создании элемента управления "дерево-представление" можно также отправить ему сообщение [**WM \_ сетфонт**](/windows/desktop/winmsg/wm-setfont) , чтобы задать шрифт, используемый для текста.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="ccfd3-119">Перед вставкой элементов необходимо отправить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="ccfd3-120">По умолчанию в представлении в виде дерева используется шрифт заголовка значка.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="ccfd3-121">Хотя можно настроить шрифт для каждого элемента с помощью [пользовательской прорисовки](custom-draw.md), элемент управления "представление в виде дерева" использует размеры шрифта, указанного в сообщении **WM \_ сетфонт** , для определения расстояния и макета.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccfd3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ccfd3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccfd3-123">Использование элементов управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="ccfd3-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="ccfd3-124">Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="ccfd3-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 