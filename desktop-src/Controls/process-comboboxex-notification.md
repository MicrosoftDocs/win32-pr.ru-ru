---
title: Обработка уведомлений ComboBoxEx
description: В этом разделе показано, как обрабатывать сообщения уведомления ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988031"
---
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="d340f-103">Обработка уведомлений ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="d340f-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="d340f-104">В этом разделе показано, как обрабатывать сообщения уведомления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="d340f-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d340f-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="d340f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d340f-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="d340f-106">Technologies</span></span>

-   [<span data-ttu-id="d340f-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="d340f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d340f-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d340f-108">Prerequisites</span></span>

-   <span data-ttu-id="d340f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="d340f-109">C/C++</span></span>
-   <span data-ttu-id="d340f-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="d340f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d340f-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="d340f-111">Instructions</span></span>


<span data-ttu-id="d340f-112">Элемент управления ComboBoxEx уведомляет свое родительское окно о событиях, отправляя сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d340f-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="d340f-113">Он также передает сообщения [**\_ командной строки WM**](/windows/desktop/menurc/wm-command) , которые он получает из поля со списком, содержащегося в нем, в родительское окно для обработки.</span><span class="sxs-lookup"><span data-stu-id="d340f-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="d340f-114">Поэтому приложение должно быть подготовлено к обработке сообщений **WM \_ Notify** из **\_ командных** сообщений ComboBoxEx и WM, пересылаемых из элемента управления дочернего поля ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="d340f-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="d340f-115">Пример в этом разделе обрабатывает сообщения [**\_ командной строки**](/windows/desktop/menurc/wm-command) [**WM \_ Notify**](wm-notify.md) и WM из элемента управления ComboBoxEx, вызывая соответствующую определяемую приложением функцию для обработки этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d340f-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="d340f-116">Полный пример</span><span class="sxs-lookup"><span data-stu-id="d340f-116">Complete example</span></span>


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="d340f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d340f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d340f-118">Сведения об элементах управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="d340f-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="d340f-119">Справочник по элементу управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="d340f-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d340f-120">Использование элементов управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="d340f-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="d340f-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="d340f-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 