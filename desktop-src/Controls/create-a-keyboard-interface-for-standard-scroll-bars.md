---
title: Создание интерфейса клавиатуры для стандартных полос прокрутки
description: Хотя элемент управления "полоса прокрутки" предоставляет встроенный интерфейс клавиатуры, стандартная полоса прокрутки не предусмотрена.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891128"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="e74e0-103">Создание интерфейса клавиатуры для стандартных полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="e74e0-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="e74e0-104">Хотя элемент управления "полоса прокрутки" предоставляет встроенный интерфейс клавиатуры, стандартная полоса прокрутки не предусмотрена.</span><span class="sxs-lookup"><span data-stu-id="e74e0-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="e74e0-105">Чтобы реализовать интерфейс клавиатуры для стандартной полосы прокрутки, процедура окна должна обработать сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) и изучить код виртуального ключа, указанный параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e74e0-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="e74e0-106">Если код виртуального ключа соответствует клавише со стрелкой, то процедура окна отправляет сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) с младшим словом параметра *wParam* , установленным в соответствующий код запроса полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e74e0-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="e74e0-107">Например, когда пользователь нажимает клавишу со стрелкой вверх, процедура окна получает сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) с параметром *wParam* , равным VK \_ up.</span><span class="sxs-lookup"><span data-stu-id="e74e0-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="e74e0-108">В ответ процедура окна отправляет сообщение [**WM \_ VSCROLL**](wm-vscroll.md) с неупорядоченным словом *wParam* , установленным в \_ код запроса SB.</span><span class="sxs-lookup"><span data-stu-id="e74e0-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e74e0-109">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e74e0-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e74e0-110">Технологии</span><span class="sxs-lookup"><span data-stu-id="e74e0-110">Technologies</span></span>

-   [<span data-ttu-id="e74e0-111">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="e74e0-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e74e0-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e74e0-112">Prerequisites</span></span>

-   <span data-ttu-id="e74e0-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="e74e0-113">C/C++</span></span>
-   <span data-ttu-id="e74e0-114">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="e74e0-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e74e0-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e74e0-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="e74e0-116">Создание интерфейса клавиатуры для стандартной полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="e74e0-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="e74e0-117">В следующем примере кода показано, как включить интерфейс клавиатуры для стандартной полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e74e0-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="e74e0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e74e0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74e0-119">Использование полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="e74e0-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="e74e0-120">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="e74e0-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 