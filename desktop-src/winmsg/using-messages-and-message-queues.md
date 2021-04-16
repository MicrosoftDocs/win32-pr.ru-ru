---
description: В следующих примерах кода показано, как выполнять следующие задачи, связанные с сообщениями Windows и очередями сообщений.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Использование сообщений и очередей сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656611"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="d5151-103">Использование сообщений и очередей сообщений</span><span class="sxs-lookup"><span data-stu-id="d5151-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="d5151-104">В следующих примерах кода показано, как выполнять следующие задачи, связанные с сообщениями Windows и очередями сообщений.</span><span class="sxs-lookup"><span data-stu-id="d5151-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="d5151-105">Создание цикла обработки сообщений</span><span class="sxs-lookup"><span data-stu-id="d5151-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="d5151-106">Проверка очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="d5151-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="d5151-107">Публикация сообщения</span><span class="sxs-lookup"><span data-stu-id="d5151-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="d5151-108">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="d5151-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="d5151-109">Создание цикла обработки сообщений</span><span class="sxs-lookup"><span data-stu-id="d5151-109">Creating a Message Loop</span></span>

<span data-ttu-id="d5151-110">Система не создает очередь сообщений для каждого потока автоматически.</span><span class="sxs-lookup"><span data-stu-id="d5151-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="d5151-111">Вместо этого система создает очередь сообщений только для потоков, выполняющих операции, для которых требуется очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="d5151-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="d5151-112">Если поток создает одно или несколько окон, необходимо предоставить цикл обработки сообщений. Этот цикл сообщений извлекает сообщения из очереди сообщений потока и отправляет их в соответствующие процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="d5151-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="d5151-113">Поскольку система направляет сообщения в отдельные окна приложения, поток должен создать по крайней мере одно окно перед началом цикла обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="d5151-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="d5151-114">Большинство приложений содержат один поток, который создает Windows.</span><span class="sxs-lookup"><span data-stu-id="d5151-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="d5151-115">Типичное приложение регистрирует класс окна для своего главного окна, создает и отображает главное окно, а затем запускает цикл обработки сообщений — все в функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="d5151-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="d5151-116">Цикл обработки сообщений создается с помощью функций [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) и [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) .</span><span class="sxs-lookup"><span data-stu-id="d5151-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="d5151-117">Если приложение должно получать символьные данные от пользователя, включите функцию [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) в цикл.</span><span class="sxs-lookup"><span data-stu-id="d5151-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="d5151-118">**TranslateMessage** преобразует сообщения виртуального ключа в символьные сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5151-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="d5151-119">В следующем примере показан цикл обработки сообщений в функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) простого приложения на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="d5151-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="d5151-120">В следующем примере показан цикл обработки сообщений для потока, который использует ускорители и отображает немодальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d5151-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="d5151-121">Когда [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) или [**Исдиалогмессаже**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) возвращает **значение true** (указывающее, что сообщение было обработано), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) и [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) не вызываются.</span><span class="sxs-lookup"><span data-stu-id="d5151-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="d5151-122">Причина в том, что **TranslateAccelerator** и **исдиалогмессаже** выполняют все необходимые преобразования и диспетчеризации сообщений.</span><span class="sxs-lookup"><span data-stu-id="d5151-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="d5151-123">Проверка очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="d5151-123">Examining a Message Queue</span></span>

<span data-ttu-id="d5151-124">Иногда приложению необходимо проверить содержимое очереди сообщений потока за пределами цикла обработки сообщений потока.</span><span class="sxs-lookup"><span data-stu-id="d5151-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="d5151-125">Например, если процедура окна приложения выполняет длительную операцию рисования, может потребоваться, чтобы пользователь мог прерывать операцию.</span><span class="sxs-lookup"><span data-stu-id="d5151-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="d5151-126">Если приложение периодически не проверяет очередь сообщений во время операции для сообщений мыши и клавиатуры, оно не реагирует на ввод пользователя до тех пор, пока не будет выполнена операция.</span><span class="sxs-lookup"><span data-stu-id="d5151-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="d5151-127">Причина заключается в том, что функция [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) в цикле обработки сообщений потока не возвращает значение до тех пор, пока процедура окна не завершит обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5151-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="d5151-128">Для проверки очереди сообщений во время длительной операции можно использовать функцию [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="d5151-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="d5151-129">**PeekMessage** аналогичен функции "функция- [**сообщение**](/windows/win32/api/winuser/nf-winuser-getmessage) "; Оба варианта проверяют очередь сообщений на наличие сообщения, удовлетворяющего условиям фильтра, а затем копируют сообщение в структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) .</span><span class="sxs-lookup"><span data-stu-id="d5151-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="d5151-130">Основное различие между этими двумя функциями заключается **в том, что функция** noreturn не возвращает значение, пока в очередь не помещается сообщение, соответствующее условиям фильтра, тогда как **PeekMessage** возвращает немедленно, независимо от того, находится ли сообщение в очереди.</span><span class="sxs-lookup"><span data-stu-id="d5151-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="d5151-131">В следующем примере показано, как использовать [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) для проверки очереди сообщений для щелчков мыши и ввода с клавиатуры во время длительной операции.</span><span class="sxs-lookup"><span data-stu-id="d5151-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="d5151-132">Другие функции, включая [**жеткуеуестатус**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) и [**жетинпутстате**](/windows/win32/api/winuser/nf-winuser-getinputstate), также позволяют проверять содержимое очереди сообщений потока.</span><span class="sxs-lookup"><span data-stu-id="d5151-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="d5151-133">**Жеткуеуестатус** возвращает массив флагов, указывающих типы сообщений в очереди; его использование — самый быстрый способ определить, содержит ли очередь сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5151-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="d5151-134">**Жетинпутстате** возвращает **значение true** , если очередь содержит сообщения мыши или клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d5151-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="d5151-135">Обе эти функции можно использовать для определения того, содержит ли очередь сообщения, которые необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="d5151-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="d5151-136">Публикация сообщения</span><span class="sxs-lookup"><span data-stu-id="d5151-136">Posting a Message</span></span>

<span data-ttu-id="d5151-137">Сообщение можно опубликовать в очереди сообщений с помощью функции вывода [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="d5151-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="d5151-138">**Сообщение** помещает сообщение в конец очереди сообщений потока и сразу же возвращается, не дожидаясь обработки сообщения потоком.</span><span class="sxs-lookup"><span data-stu-id="d5151-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="d5151-139">Параметры функции включают в себя маркер окна, идентификатор сообщения и два параметра сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5151-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="d5151-140">Система копирует эти параметры в структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , заполняет элементы **time** и **PT** структуры и помещает структуру в очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="d5151-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="d5151-141">Система использует маркер окна, переданный функцией вывода [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) , для определения того, какая очередь сообщений потока должна принимать сообщение.</span><span class="sxs-lookup"><span data-stu-id="d5151-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="d5151-142">Если дескриптор является **HWND, \_** то система отправляет сообщение в очереди сообщений потока всех окон верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d5151-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="d5151-143">Функцию [**постсреадмессаже**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) можно использовать для публикации сообщения в конкретную очередь сообщений потока.</span><span class="sxs-lookup"><span data-stu-id="d5151-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="d5151-144">**Постсреадмессаже** похож на [**сообщение**](/windows/win32/api/winuser/nf-winuser-postmessagea), за исключением того, что первый параметр является идентификатором потока, а не обработчиком окна.</span><span class="sxs-lookup"><span data-stu-id="d5151-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="d5151-145">Идентификатор потока можно получить, вызвав функцию [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .</span><span class="sxs-lookup"><span data-stu-id="d5151-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="d5151-146">Используйте функцию [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) для выхода из цикла обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="d5151-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="d5151-147">**Посткуитмессаже** отправляет сообщение [**о \_ выходе WM Quit**](wm-quit.md) в текущий выполняемый поток.</span><span class="sxs-lookup"><span data-stu-id="d5151-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="d5151-148">Цикл обработки сообщений потока завершает работу и возвращает управление системе при обнаружении сообщения **WM \_ Quit** .</span><span class="sxs-lookup"><span data-stu-id="d5151-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="d5151-149">Приложение обычно вызывает **посткуитмессаже** в ответ на сообщение [**WM \_ destroy**](wm-destroy.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d5151-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="d5151-150">Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="d5151-150">Sending a Message</span></span>

<span data-ttu-id="d5151-151">Функция [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) используется для отправки сообщения непосредственно в процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="d5151-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="d5151-152">**SendMessage** вызывает процедуру окна и ожидает, пока эта процедура обработает сообщение и возвращало результат.</span><span class="sxs-lookup"><span data-stu-id="d5151-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="d5151-153">Сообщение может быть отправлено в любое окно в системе; все, что требуется, — это обработчик окна.</span><span class="sxs-lookup"><span data-stu-id="d5151-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="d5151-154">Система использует этот обработчик, чтобы определить, какая именно оконная процедура должна получить сообщение.</span><span class="sxs-lookup"><span data-stu-id="d5151-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="d5151-155">Перед обработкой сообщения, которое могло быть отправлено из другого потока, процедура окна должна сначала вызвать функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) .</span><span class="sxs-lookup"><span data-stu-id="d5151-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="d5151-156">Если эта функция возвращает **значение true**, то процедура Window должна вызывать [**реплимессаже**](/windows/win32/api/winuser/nf-winuser-replymessage) перед любой функцией, которая приводит к передаче управления потоком, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d5151-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="d5151-157">В диалоговом окне можно отправлять несколько сообщений в элементы управления.</span><span class="sxs-lookup"><span data-stu-id="d5151-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="d5151-158">Эти управляющие сообщения устанавливают внешний вид, поведение и содержимое элементов управления или извлекают сведения об элементах управления.</span><span class="sxs-lookup"><span data-stu-id="d5151-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="d5151-159">Например, сообщение [**\_ ADDSTRING CB**](../controls/cb-addstring.md) может добавлять строку в поле со списком, а сообщение [**\_ сетчекк BM**](../controls/bm-setcheck.md) может устанавливать состояние флажка или переключателя.</span><span class="sxs-lookup"><span data-stu-id="d5151-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="d5151-160">Используйте функцию [**сенддлгитеммессаже**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) для отправки сообщения в элемент управления, указав идентификатор элемента управления и маркер окна диалогового окна, содержащего этот элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d5151-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="d5151-161">Следующий пример, взятый из процедуры диалогового окна, копирует строку из элемента управления "поле со списком" в его список.</span><span class="sxs-lookup"><span data-stu-id="d5151-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="d5151-162">В примере **сенддлгитеммессаже** используется для отправки сообщения [**\_ ADDSTRING CB**](../controls/cb-addstring.md) в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="d5151-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
