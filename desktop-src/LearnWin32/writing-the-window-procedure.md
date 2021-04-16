---
title: Написание процедуры окна
description: .
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f11b22ba5dd0653905ca4e2bdb546d106183fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672265"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="30429-103">Написание процедуры окна</span><span class="sxs-lookup"><span data-stu-id="30429-103">Writing the Window Procedure</span></span>

<span data-ttu-id="30429-104">Функция [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) вызывает процедуру окна, которая является целью сообщения.</span><span class="sxs-lookup"><span data-stu-id="30429-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="30429-105">Процедура окна имеет следующую сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="30429-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="30429-106">Существует четыре параметра:</span><span class="sxs-lookup"><span data-stu-id="30429-106">There are four parameters:</span></span>

- <span data-ttu-id="30429-107">*HWND* — это дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="30429-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="30429-108">*uiacp* — это код сообщения; Например, сообщение с [**\_ размером WM**](/windows/desktop/winmsg/wm-size) указывает, что размер окна был изменен.</span><span class="sxs-lookup"><span data-stu-id="30429-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="30429-109">*wParam* и *lParam* содержат дополнительные данные, относящиеся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="30429-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="30429-110">Точное значение зависит от кода сообщения.</span><span class="sxs-lookup"><span data-stu-id="30429-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="30429-111">**LResult** — это целочисленное значение, которое программа возвращает в Windows.</span><span class="sxs-lookup"><span data-stu-id="30429-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="30429-112">Он содержит ответ программы на определенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="30429-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="30429-113">Значение этого параметра зависит от кода сообщения.</span><span class="sxs-lookup"><span data-stu-id="30429-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="30429-114">**Обратный вызов** — это соглашение о вызовах для функции.</span><span class="sxs-lookup"><span data-stu-id="30429-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="30429-115">Типичная процедура окна — это просто большой оператор switch, который переключается на код сообщения.</span><span class="sxs-lookup"><span data-stu-id="30429-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="30429-116">Добавьте варианты для каждого сообщения, которое требуется обработать.</span><span class="sxs-lookup"><span data-stu-id="30429-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="30429-117">Дополнительные данные для сообщения содержатся в параметрах *lParam* и *wParam* .</span><span class="sxs-lookup"><span data-stu-id="30429-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="30429-118">Оба параметра — это целочисленные значения, размер которых равен ширине указателя (32 бит или 64 бит).</span><span class="sxs-lookup"><span data-stu-id="30429-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="30429-119">Значение каждого из них зависит от кода сообщения (*uiacp*).</span><span class="sxs-lookup"><span data-stu-id="30429-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="30429-120">Для каждого сообщения необходимо найти код сообщения в MSDN и привести параметры к правильному типу данных.</span><span class="sxs-lookup"><span data-stu-id="30429-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="30429-121">Обычно данные представляют собой числовое значение или указатель на структуру.</span><span class="sxs-lookup"><span data-stu-id="30429-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="30429-122">Некоторые сообщения не содержат данных.</span><span class="sxs-lookup"><span data-stu-id="30429-122">Some messages do not have any data.</span></span>

<span data-ttu-id="30429-123">Например, документация для сообщения о [**\_ размере WM**](/windows/desktop/winmsg/wm-size) сообщает, что:</span><span class="sxs-lookup"><span data-stu-id="30429-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="30429-124">*wParam* — это флаг, указывающий, было ли окно сведено, развернуто или изменено его размер.</span><span class="sxs-lookup"><span data-stu-id="30429-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="30429-125">*lParam* содержит новую ширину и высоту окна в виде 16-разрядных значений, упакованных в 1 32 или 64-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="30429-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="30429-126">Для получения этих значений необходимо выполнить некоторую побитовую смену.</span><span class="sxs-lookup"><span data-stu-id="30429-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="30429-127">К счастью, файл заголовка Виндеф. h содержит вспомогательные макросы, которые делают это.</span><span class="sxs-lookup"><span data-stu-id="30429-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="30429-128">Типичная процедура окна обрабатывает десятки сообщений, поэтому она может увеличиваться довольно долго.</span><span class="sxs-lookup"><span data-stu-id="30429-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="30429-129">Одним из способов сделать код более модульным является помещение логики обработки каждого сообщения в отдельную функцию.</span><span class="sxs-lookup"><span data-stu-id="30429-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="30429-130">В окне процедуры приведите параметры *wParam* и *lParam* к правильному типу данных и передайте эти значения в функцию.</span><span class="sxs-lookup"><span data-stu-id="30429-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="30429-131">Например, для обработки сообщения с [**\_ размером WM**](/windows/desktop/winmsg/wm-size) процедура окна будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="30429-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

<span data-ttu-id="30429-132">Макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) получают 16-разрядные значения ширины и высоты из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="30429-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="30429-133">(Эти сведения можно найти в документации MSDN по каждому коду сообщения.) Процедура окна извлекает ширину и высоту, а затем передает эти значения в `OnSize` функцию.</span><span class="sxs-lookup"><span data-stu-id="30429-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="30429-134">Обработка сообщений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="30429-134">Default Message Handling</span></span>

<span data-ttu-id="30429-135">Если вы не обрабатываете конкретное сообщение в процедуре окна, передайте параметры сообщения непосредственно в функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="30429-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="30429-136">Эта функция выполняет действие по умолчанию для сообщения, которое зависит от типа сообщения.</span><span class="sxs-lookup"><span data-stu-id="30429-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="30429-137">Предотвращение узких мест в процедуре окна</span><span class="sxs-lookup"><span data-stu-id="30429-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="30429-138">Во время выполнения процедуры окна она блокирует любые другие сообщения для Windows, созданные в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="30429-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="30429-139">Поэтому следует избегать длительной обработки внутри процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="30429-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="30429-140">Например, предположим, что программа открывает TCP-соединение и ожидает ответа сервера на неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="30429-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="30429-141">Если сделать это внутри процедуры окна, Пользовательский интерфейс не будет отвечать, пока запрос не завершится.</span><span class="sxs-lookup"><span data-stu-id="30429-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="30429-142">В течение этого времени окно не может обрабатывать ввод, перерисовку или даже закрытие окна с помощью мыши или клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="30429-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="30429-143">Вместо этого следует переместить работу в другой поток, используя один из многозадачных средств, встроенных в Windows:</span><span class="sxs-lookup"><span data-stu-id="30429-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="30429-144">Создание нового потока.</span><span class="sxs-lookup"><span data-stu-id="30429-144">Create a new thread.</span></span>
- <span data-ttu-id="30429-145">Использование пула потоков.</span><span class="sxs-lookup"><span data-stu-id="30429-145">Use a thread pool.</span></span>
- <span data-ttu-id="30429-146">Используйте асинхронные вызовы ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="30429-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="30429-147">Используйте асинхронные вызовы процедур.</span><span class="sxs-lookup"><span data-stu-id="30429-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="30429-148">Следующая</span><span class="sxs-lookup"><span data-stu-id="30429-148">Next</span></span>

[<span data-ttu-id="30429-149">Рисование окна</span><span class="sxs-lookup"><span data-stu-id="30429-149">Painting the Window</span></span>](painting-the-window.md)