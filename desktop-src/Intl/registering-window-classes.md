---
description: Класс окна поддерживается процедурой окна. Приложение может зарегистрировать класс окна с помощью при или Регистерклассв. Новые приложения обычно используют Регистерклассв.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Регистрация классов Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f508ebdbfa35f2551d723b3ef9a1ffd807917dfe71e503f9d77b2e8fdb136f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040454"
---
# <a name="registering-window-classes"></a>Регистрация классов Window

Класс окна поддерживается процедурой окна. Приложение может зарегистрировать класс окна с помощью [**при**](/windows/win32/api/winuser/nf-winuser-registerclassa) или [**регистерклассв**](/windows/win32/api/winuser/nf-winuser-registerclassa). Новые приложения обычно используют **регистерклассв**.

если приложение регистрирует класс окна с помощью [**при**](/windows/win32/api/winuser/nf-winuser-registerclassa), функция информирует операционную систему о том, что окна созданного класса задают сообщения с текстовыми или символьными параметрами для использования кодировки [кодовой страницы Windows (ANSI)](code-pages.md) . Регистрация с помощью [**регистерклассв**](/windows/win32/api/winuser/nf-winuser-registerclassa) позволяет приложению запросить операционную систему для передачи текстовых параметров сообщений в [Юникоде](unicode.md). Функция [**исвиндовуникоде**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) позволяет приложению запрашивать характер каждого окна.

в следующем примере показано, как зарегистрировать класс окна кодовой страницы Windows и класс окна с поддержкой юникода, а также как написать процедуры окна для обоих вариантов. В этом примере все функции и структуры отображаются с конкретными типами данных "A" (ANSI) или "W" (Wide, Юникод). используя методы, описанные в разделах [использование универсальных типов данных](using-generic-data-types.md), можно также написать этот пример для использования универсальных типов данных, чтобы его можно было компилировать для использования либо Windows кодовых страниц, либо юникода в зависимости от того, определено ли значение "unicode".


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



в следующем примере показано различие между обработкой сообщения [**WM \_ CHAR**](../inputdev/wm-char.md) в Windows процедуре окна кодовой страницы и процедурой окна юникода.


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



весь текст в сообщениях, полученных **ансивндпрок** , состоит из Windows символов кодовой страницы. Весь текст в сообщениях, полученных **унивндпрок** , состоит из символов Юникода.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Юникода и кодировок](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
