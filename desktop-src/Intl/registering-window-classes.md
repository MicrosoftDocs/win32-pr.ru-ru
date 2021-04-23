---
description: Класс окна поддерживается процедурой окна. Приложение может зарегистрировать класс окна с помощью при или Регистерклассв. Новые приложения обычно используют Регистерклассв.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Регистрация классов Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156887"
---
# <a name="registering-window-classes"></a><span data-ttu-id="99d21-105">Регистрация классов Window</span><span class="sxs-lookup"><span data-stu-id="99d21-105">Registering Window Classes</span></span>

<span data-ttu-id="99d21-106">Класс окна поддерживается процедурой окна.</span><span class="sxs-lookup"><span data-stu-id="99d21-106">A window class is supported by a window procedure.</span></span> <span data-ttu-id="99d21-107">Приложение может зарегистрировать класс окна с помощью [**при**](/windows/win32/api/winuser/nf-winuser-registerclassa) или [**регистерклассв**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="99d21-107">Your application can register a window class by using either [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) or [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="99d21-108">Новые приложения обычно используют **регистерклассв**.</span><span class="sxs-lookup"><span data-stu-id="99d21-108">New applications should typically use **RegisterClassW**.</span></span>

<span data-ttu-id="99d21-109">Если приложение регистрирует класс окна с помощью [**при**](/windows/win32/api/winuser/nf-winuser-registerclassa), функция информирует операционную систему о том, что окна созданного класса задают сообщения с текстовыми или символьными параметрами для использования кодировки [кодовой страницы Windows (ANSI)](code-pages.md) .</span><span class="sxs-lookup"><span data-stu-id="99d21-109">If the application registers the window class using [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), the function informs the operating system that the windows of the created class expect messages with text or character parameters to use a [Windows (ANSI) code page](code-pages.md) character set.</span></span> <span data-ttu-id="99d21-110">Регистрация с помощью [**регистерклассв**](/windows/win32/api/winuser/nf-winuser-registerclassa) позволяет приложению запросить операционную систему для передачи текстовых параметров сообщений в [Юникоде](unicode.md).</span><span class="sxs-lookup"><span data-stu-id="99d21-110">Registration using [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) allows the application to request the operating system to pass text parameters of messages as [Unicode](unicode.md).</span></span> <span data-ttu-id="99d21-111">Функция [**исвиндовуникоде**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) позволяет приложению запрашивать характер каждого окна.</span><span class="sxs-lookup"><span data-stu-id="99d21-111">The [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) function enables an application to query the nature of each window.</span></span>

<span data-ttu-id="99d21-112">В следующем примере показано, как зарегистрировать класс окна кодовой страницы Windows и класс окна в Юникоде и как написать процедуры окна для обоих вариантов.</span><span class="sxs-lookup"><span data-stu-id="99d21-112">The following example shows how to register a Windows code page window class and a Unicode window class and how to write the window procedures for both cases.</span></span> <span data-ttu-id="99d21-113">В этом примере все функции и структуры отображаются с конкретными типами данных "A" (ANSI) или "W" (Wide, Юникод).</span><span class="sxs-lookup"><span data-stu-id="99d21-113">For the purposes of this example, all functions and structures are shown with the specific "A" (ANSI) or "W" (wide, Unicode) data types.</span></span> <span data-ttu-id="99d21-114">Используя методы, описанные в разделах [Использование универсальных типов данных](using-generic-data-types.md), можно также написать этот пример для использования универсальных типов данных, чтобы его можно было компилировать для использования кодовых страниц Windows или Юникода в зависимости от того, определено ли значение "Unicode".</span><span class="sxs-lookup"><span data-stu-id="99d21-114">Using the techniques explained in [Using Generic Data Types](using-generic-data-types.md), you can alternatively write this example to use generic data types, so that it can be compiled to use either Windows code pages or Unicode, depending on whether "UNICODE" is defined.</span></span>


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



<span data-ttu-id="99d21-115">В следующем примере показано различие между обработкой сообщения [**WM \_ char**](../inputdev/wm-char.md) в процедуре окна кодовой страницы Windows и процедурой окна Юникода.</span><span class="sxs-lookup"><span data-stu-id="99d21-115">The following example shows the difference between handling the [**WM\_CHAR**](../inputdev/wm-char.md) message in a Windows code page window procedure and a Unicode window procedure.</span></span>


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



<span data-ttu-id="99d21-116">Весь текст в сообщениях, полученных **ансивндпрок** , состоит из символов кодовой страницы Windows.</span><span class="sxs-lookup"><span data-stu-id="99d21-116">All text in messages received by **AnsiWndProc** is composed of Windows code page characters.</span></span> <span data-ttu-id="99d21-117">Весь текст в сообщениях, полученных **унивндпрок** , состоит из символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="99d21-117">All text in messages received by **UniWndProc** is composed of Unicode characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99d21-118">См. также</span><span class="sxs-lookup"><span data-stu-id="99d21-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d21-119">Использование Юникода и кодировок</span><span class="sxs-lookup"><span data-stu-id="99d21-119">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
