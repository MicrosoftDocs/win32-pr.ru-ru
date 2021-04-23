---
title: Закрытие окна
description: Когда пользователь закрывает окно, это действие запускает последовательность сообщений окна.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890656"
---
# <a name="closing-the-window"></a><span data-ttu-id="da6ea-103">Закрытие окна</span><span class="sxs-lookup"><span data-stu-id="da6ea-103">Closing the Window</span></span>

<span data-ttu-id="da6ea-104">Когда пользователь закрывает окно, это действие запускает последовательность сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="da6ea-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="da6ea-105">Пользователь может закрыть окно приложения, нажав кнопку **Закрыть** или воспользовавшись сочетанием клавиш, например ALT + F4.</span><span class="sxs-lookup"><span data-stu-id="da6ea-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="da6ea-106">Любое из этих действий приводит к тому, что окно получает сообщение [**\_ закрытия WM**](/windows/desktop/winmsg/wm-close) .</span><span class="sxs-lookup"><span data-stu-id="da6ea-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="da6ea-107">Сообщение **\_ закрытия WM** дает возможность запросить пользователя перед закрытием окна.</span><span class="sxs-lookup"><span data-stu-id="da6ea-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="da6ea-108">Если вы действительно хотите закрыть окно, вызовите функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="da6ea-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="da6ea-109">В противном случае просто возвращает ноль из сообщения **\_ закрытия WM** , и операционная система пропустит это сообщение и не уничтожит окно.</span><span class="sxs-lookup"><span data-stu-id="da6ea-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="da6ea-110">Ниже приведен пример того, как программа может работать с [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="da6ea-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="da6ea-111">В этом примере функция [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) показывает модальное диалоговое окно, содержащее кнопки **ОК** и **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="da6ea-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="da6ea-112">Если пользователь нажмет кнопку **ОК**, программа вызывает [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span><span class="sxs-lookup"><span data-stu-id="da6ea-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="da6ea-113">В противном случае, если пользователь нажимает кнопку **Отмена**, вызов **дестройвиндов** пропускается, а окно остается открытым.</span><span class="sxs-lookup"><span data-stu-id="da6ea-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="da6ea-114">В любом случае возвращается нуль, чтобы указать, что сообщение обработано.</span><span class="sxs-lookup"><span data-stu-id="da6ea-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="da6ea-115">Если вы хотите закрыть окно без запроса пользователя, можно просто вызвать [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) без вызова [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span><span class="sxs-lookup"><span data-stu-id="da6ea-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="da6ea-116">Однако в этом случае есть ярлык.</span><span class="sxs-lookup"><span data-stu-id="da6ea-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="da6ea-117">Помните, что [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выполняет действие по умолчанию для любого сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="da6ea-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="da6ea-118">В случае с [**WM \_ Close**](/windows/desktop/winmsg/wm-close) **дефвиндовпрок** автоматически вызывает **дестройвиндов**.</span><span class="sxs-lookup"><span data-stu-id="da6ea-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="da6ea-119">Это означает, что если вы пропускаете сообщение **\_ закрытия WM** в операторе **switch** , окно уничтожается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da6ea-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="da6ea-120">Когда окно собирается уничтожиться, оно получает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="da6ea-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="da6ea-121">Это сообщение отправляется после удаления окна с экрана, но до возникновения уничтожения (в частности, перед уничтожением дочерних окон).</span><span class="sxs-lookup"><span data-stu-id="da6ea-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="da6ea-122">В главном окне приложения вы обычно отвечаете на [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) , вызывая [**посткуитмессаже**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="da6ea-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="da6ea-123">В разделе [оконных сообщений](window-messages.md) мы видели, что [**посткуитмессаже**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) помещает в очередь сообщений сообщение [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) , что приводит к завершению цикла обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="da6ea-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="da6ea-124">Ниже приведена типичная схема обработки сообщений [**WM \_ Close**](/windows/desktop/winmsg/wm-close) и [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="da6ea-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![блок диаграмма, показывающий, как работать с \- сообщениями WM Close и WM \- destroy](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="da6ea-126">Следующая</span><span class="sxs-lookup"><span data-stu-id="da6ea-126">Next</span></span>

[<span data-ttu-id="da6ea-127">Управление состоянием приложения</span><span class="sxs-lookup"><span data-stu-id="da6ea-127">Managing Application State</span></span>](managing-application-state-.md)