---
title: Создание всплывающей подсказки для прямоугольной области
description: В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774189"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="36182-103">Создание всплывающей подсказки для прямоугольной области</span><span class="sxs-lookup"><span data-stu-id="36182-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="36182-104">В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="36182-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="36182-105">На следующем рисунке показана подсказка, которая отображается, когда указатель мыши находится в окне клиента диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="36182-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="36182-106">Маркер диалогового окна был передан функции, показанной в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="36182-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![снимок экрана: диалоговое окно; указатель мыши находится в окне клиента, и всплывающая подсказка отображается](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="36182-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="36182-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="36182-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="36182-109">Technologies</span></span>

-   [<span data-ttu-id="36182-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="36182-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="36182-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="36182-111">Prerequisites</span></span>

-   <span data-ttu-id="36182-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="36182-112">C/C++</span></span>
-   <span data-ttu-id="36182-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="36182-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="36182-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="36182-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="36182-115">Создать подсказку для прямоугольной области</span><span class="sxs-lookup"><span data-stu-id="36182-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="36182-116">В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="36182-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="36182-117">См. также</span><span class="sxs-lookup"><span data-stu-id="36182-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36182-118">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="36182-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




