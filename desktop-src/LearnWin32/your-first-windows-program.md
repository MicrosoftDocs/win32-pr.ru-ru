---
title: Модуль 1. Ваша первая программа Windows
description: Модуль 1. Ваша первая программа Windows
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110952"
---
# <a name="module-1-your-first-windows-program"></a>Модуль 1. Ваша первая программа Windows

В этом модуле мы создадим минимальную программу для Windows Desktop. Все это создает и отображает пустое окно. Первая программа содержит около 50 строк кода без учета пустых строк и комментариев. Это будет начальная точка; Позже мы добавим графические, текстовые, пользовательские данные и другие функции.

Если вам нужны дополнительные сведения о создании традиционного классического приложения Windows в Visual Studio, см.  [Пошаговое руководство. создание традиционного классического приложения Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).

![снимок экрана с примером программы](images/window01.png)

Ниже приведен полный код программы:


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





Вы можете скачать полный проект Visual Studio из [примера Hello World Windows](windows-hello-world-sample.md).

Может быть полезно дать краткий обзор того, что делает этот код. В последующих разделах подробно рассматривается код.

1.  **wWinMain** — это точка входа в программу. При запуске программа регистрирует некоторые сведения о поведении окна приложения. Одним из наиболее важных элементов является адрес функции с именем `WindowProc` в этом примере. Эта функция определяет поведение окна (его внешний вид, способ взаимодействия с пользователем и т. д.).
2.  Затем программа создает окно и получает маркер, который однозначно идентифицирует окно.
3.  Если окно создано успешно, программа вводит цикл **while** . Программа остается в этом цикле до тех пор, пока пользователь не закроет окно и не выполнит выход из приложения.

Обратите внимание, что программа не вызывает явно `WindowProc` функцию, даже если мы говорили о том, где определена большая часть логики приложения. Windows обменивается данными с программой, передавая ей серию *сообщений*. Этот процесс управляется кодом внутри цикла **while** . Каждый раз, когда программа вызывает функцию [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , она косвенно заставляет Windows вызывать функцию WindowProc по одному разу для каждого сообщения.

## <a name="in-this-section"></a>Содержание раздела

-   [Создание окна](creating-a-window.md)
-   [Сообщения окна](window-messages.md)
-   [Написание процедуры окна](writing-the-window-procedure.md)
-   [Рисование окна](painting-the-window.md)
-   [Закрытие окна](closing-the-window.md)
-   [Управление состоянием приложения](managing-application-state-.md)

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Знакомство с программой для Windows в C++](learn-to-program-for-windows.md)
</dt> <dt>

[Пример Hello World Windows](windows-hello-world-sample.md)
</dt> </dl>

 

 
