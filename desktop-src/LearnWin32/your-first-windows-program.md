---
title: Модуль 1. Ваша первая программа Windows
description: .
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27749cddabaefb4fd83b836887fbb2dac017d238
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "104563902"
---
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="9a905-104">Модуль 1.</span><span class="sxs-lookup"><span data-stu-id="9a905-104">Module 1.</span></span> <span data-ttu-id="9a905-105">Ваша первая программа Windows</span><span class="sxs-lookup"><span data-stu-id="9a905-105">Your First Windows Program</span></span>

<span data-ttu-id="9a905-106">В этом модуле мы создадим минимальную программу для Windows Desktop.</span><span class="sxs-lookup"><span data-stu-id="9a905-106">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="9a905-107">Все это создает и отображает пустое окно.</span><span class="sxs-lookup"><span data-stu-id="9a905-107">All it does is create and show a blank window.</span></span> <span data-ttu-id="9a905-108">Первая программа содержит около 50 строк кода без учета пустых строк и комментариев.</span><span class="sxs-lookup"><span data-stu-id="9a905-108">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="9a905-109">Это будет начальная точка; Позже мы добавим графические, текстовые, пользовательские данные и другие функции.</span><span class="sxs-lookup"><span data-stu-id="9a905-109">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="9a905-110">Если вам нужны дополнительные сведения о создании традиционного классического приложения Windows в Visual Studio, см.  [Пошаговое руководство. создание традиционного классического приложения Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="9a905-110">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![снимок экрана с примером программы](images/window01.png)

<span data-ttu-id="9a905-112">Ниже приведен полный код программы:</span><span class="sxs-lookup"><span data-stu-id="9a905-112">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="9a905-113">Вы можете скачать полный проект Visual Studio из [примера Hello World Windows](windows-hello-world-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9a905-113">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="9a905-114">Может быть полезно дать краткий обзор того, что делает этот код.</span><span class="sxs-lookup"><span data-stu-id="9a905-114">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="9a905-115">В последующих разделах подробно рассматривается код.</span><span class="sxs-lookup"><span data-stu-id="9a905-115">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="9a905-116">**wWinMain** — это точка входа в программу.</span><span class="sxs-lookup"><span data-stu-id="9a905-116">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="9a905-117">При запуске программа регистрирует некоторые сведения о поведении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="9a905-117">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="9a905-118">Одним из наиболее важных элементов является адрес функции с именем `WindowProc` в этом примере.</span><span class="sxs-lookup"><span data-stu-id="9a905-118">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="9a905-119">Эта функция определяет поведение окна (его внешний вид, способ взаимодействия с пользователем и т. д.).</span><span class="sxs-lookup"><span data-stu-id="9a905-119">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="9a905-120">Затем программа создает окно и получает маркер, который однозначно идентифицирует окно.</span><span class="sxs-lookup"><span data-stu-id="9a905-120">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="9a905-121">Если окно создано успешно, программа вводит цикл **while** .</span><span class="sxs-lookup"><span data-stu-id="9a905-121">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="9a905-122">Программа остается в этом цикле до тех пор, пока пользователь не закроет окно и не выполнит выход из приложения.</span><span class="sxs-lookup"><span data-stu-id="9a905-122">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="9a905-123">Обратите внимание, что программа не вызывает явно `WindowProc` функцию, даже если мы говорили о том, где определена большая часть логики приложения.</span><span class="sxs-lookup"><span data-stu-id="9a905-123">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="9a905-124">Windows обменивается данными с программой, передавая ей серию *сообщений*.</span><span class="sxs-lookup"><span data-stu-id="9a905-124">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="9a905-125">Этот процесс управляется кодом внутри цикла **while** .</span><span class="sxs-lookup"><span data-stu-id="9a905-125">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="9a905-126">Каждый раз, когда программа вызывает функцию [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) , она косвенно заставляет Windows вызывать функцию WindowProc по одному разу для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9a905-126">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9a905-127">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="9a905-127">In this section</span></span>

-   [<span data-ttu-id="9a905-128">Создание окна</span><span class="sxs-lookup"><span data-stu-id="9a905-128">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="9a905-129">Сообщения окна</span><span class="sxs-lookup"><span data-stu-id="9a905-129">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="9a905-130">Написание процедуры окна</span><span class="sxs-lookup"><span data-stu-id="9a905-130">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="9a905-131">Рисование окна</span><span class="sxs-lookup"><span data-stu-id="9a905-131">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="9a905-132">Закрытие окна</span><span class="sxs-lookup"><span data-stu-id="9a905-132">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="9a905-133">Управление состоянием приложения</span><span class="sxs-lookup"><span data-stu-id="9a905-133">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="9a905-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9a905-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a905-135">Знакомство с программой для Windows в C++</span><span class="sxs-lookup"><span data-stu-id="9a905-135">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="9a905-136">Пример Hello World Windows</span><span class="sxs-lookup"><span data-stu-id="9a905-136">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
