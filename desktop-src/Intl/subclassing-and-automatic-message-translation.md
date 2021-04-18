---
description: Создание подклассов — это метод, позволяющий приложению перехватывать и обрабатывать сообщения, отправленные или отправляемые в определенное окно, прежде чем процедура окна сможет их обработать.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Подклассы и автоматическое преобразование сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683841"
---
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="1a50f-103">Подклассы и автоматическое преобразование сообщений</span><span class="sxs-lookup"><span data-stu-id="1a50f-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="1a50f-104">Создание подклассов — это метод, позволяющий приложению перехватывать и обрабатывать сообщения, отправленные или отправляемые в определенное окно, прежде чем процедура окна сможет их обработать.</span><span class="sxs-lookup"><span data-stu-id="1a50f-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="1a50f-105">Операционная система автоматически преобразует сообщения в [кодовую страницу Windows (ANSI)](code-pages.md) или в форму [Юникода](unicode.md) в зависимости от формы функции, которая подклассировать процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="1a50f-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="1a50f-106">Следующий вызов функции [**сетвиндовлонга**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) подклассировать текущую процедуру окна, связанную с окном, определяемым параметром *HWND* .</span><span class="sxs-lookup"><span data-stu-id="1a50f-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="1a50f-107">Кроме того, приложение может использовать [**сетвиндовлонгптра**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span><span class="sxs-lookup"><span data-stu-id="1a50f-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="1a50f-108">Новая процедура окна **неввндпрок**, получит сообщения с текстом в формате кодовой страницы Windows.</span><span class="sxs-lookup"><span data-stu-id="1a50f-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="1a50f-109">Когда **неввндпрок** заканчивает обработку сообщения, он использует функцию [**каллвиндовпрок**](/windows/win32/api/winuser/nf-winuser-callwindowproca) следующим образом для передачи сообщения в **олдвндпрок**.</span><span class="sxs-lookup"><span data-stu-id="1a50f-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="1a50f-110">Если **олдвндпрок** был создан с использованием стиля класса Unicode, сообщения транслируются из формы кодовой страницы Windows, полученной из **неввндпрок** в Юникод.</span><span class="sxs-lookup"><span data-stu-id="1a50f-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="1a50f-111">Аналогичным образом, вызов функции [**сетвиндовлонгв**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) или [**сетвиндовлонгптрв**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) подклассировать текущую процедуру окна с процедурой окна, ожидающей текстовые сообщения в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1a50f-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="1a50f-112">При необходимости преобразование сообщения выполняется во время обработки функции [**каллвиндовпрок**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="1a50f-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="1a50f-113">Дополнительные сведения о подклассах см. в разделе [процедуры окна](../winmsg/window-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="1a50f-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a50f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="1a50f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a50f-115">Использование Юникода и кодировок</span><span class="sxs-lookup"><span data-stu-id="1a50f-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
