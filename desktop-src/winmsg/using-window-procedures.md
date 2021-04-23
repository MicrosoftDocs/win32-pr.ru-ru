---
description: В этом разделе описывается выполнение следующих задач, связанных с процедурами окон.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Использование оконных процедур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912608"
---
# <a name="using-window-procedures"></a><span data-ttu-id="ef342-103">Использование оконных процедур</span><span class="sxs-lookup"><span data-stu-id="ef342-103">Using Window Procedures</span></span>

<span data-ttu-id="ef342-104">В этом разделе описывается выполнение следующих задач, связанных с процедурами окон.</span><span class="sxs-lookup"><span data-stu-id="ef342-104">This section explains how to perform the following tasks associated with window procedures.</span></span>

-   [<span data-ttu-id="ef342-105">Разработка процедуры окна</span><span class="sxs-lookup"><span data-stu-id="ef342-105">Designing a Window Procedure</span></span>](#designing-a-window-procedure)
-   [<span data-ttu-id="ef342-106">Связывание оконной процедуры с классом окна</span><span class="sxs-lookup"><span data-stu-id="ef342-106">Associating a Window Procedure with a Window Class</span></span>](#associating-a-window-procedure-with-a-window-class)
-   [<span data-ttu-id="ef342-107">Подклассировать окно</span><span class="sxs-lookup"><span data-stu-id="ef342-107">Subclassing a Window</span></span>](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a><span data-ttu-id="ef342-108">Разработка процедуры окна</span><span class="sxs-lookup"><span data-stu-id="ef342-108">Designing a Window Procedure</span></span>

<span data-ttu-id="ef342-109">В следующем примере показана структура типичной процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-109">The following example shows the structure of a typical window procedure.</span></span> <span data-ttu-id="ef342-110">В процедуре окна используется аргумент Message в операторе **switch** с отдельными сообщениями, обрабатываемыми отдельными инструкциями **case** .</span><span class="sxs-lookup"><span data-stu-id="ef342-110">The window procedure uses the message argument in a **switch** statement with individual messages handled by separate **case** statements.</span></span> <span data-ttu-id="ef342-111">Обратите внимание, что каждый вариант возвращает определенное значение для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef342-111">Notice that each case returns a specific value for each message.</span></span> <span data-ttu-id="ef342-112">Для сообщений, которые не обрабатываются, процедура Window вызывает функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="ef342-112">For messages that it does not process, the window procedure calls the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



<span data-ttu-id="ef342-113">Сообщение [**WM \_ нккреате**](wm-nccreate.md) отправляется сразу после создания окна, но если приложение отвечает на это сообщение, возвращая **значение false**, функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ef342-113">The [**WM\_NCCREATE**](wm-nccreate.md) message is sent just after your window is created, but if an application responds to this message by returning **FALSE**, [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function fails.</span></span> <span data-ttu-id="ef342-114">Сообщение [**о \_ создании WM**](wm-create.md) отправляется после того, как окно уже создано.</span><span class="sxs-lookup"><span data-stu-id="ef342-114">The [**WM\_CREATE**](wm-create.md) message is sent after your window is already created.</span></span>

<span data-ttu-id="ef342-115">Сообщение [**WM \_ destroy**](wm-destroy.md) отправляется, когда окно собирается уничтожиться.</span><span class="sxs-lookup"><span data-stu-id="ef342-115">The [**WM\_DESTROY**](wm-destroy.md) message is sent when your window is about to be destroyed.</span></span> <span data-ttu-id="ef342-116">Функция [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) выполняет удаление всех дочерних окон удаляемого окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-116">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function takes care of destroying any child windows of the window being destroyed.</span></span> <span data-ttu-id="ef342-117">Сообщение [**WM \_ нкдестрой**](wm-ncdestroy.md) отправляется непосредственно перед уничтожением окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-117">The [**WM\_NCDESTROY**](wm-ncdestroy.md) message is sent just before a window is destroyed.</span></span>

<span data-ttu-id="ef342-118">Как минимум, процедура окна должна обрабатывать сообщение [**WM \_ Paint**](../gdi/wm-paint.md) для рисования самого себя.</span><span class="sxs-lookup"><span data-stu-id="ef342-118">At the very least, a window procedure should process the [**WM\_PAINT**](../gdi/wm-paint.md) message to draw itself.</span></span> <span data-ttu-id="ef342-119">Обычно он также обрабатывает сообщения мыши и клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ef342-119">Typically, it should handle mouse and keyboard messages as well.</span></span> <span data-ttu-id="ef342-120">Ознакомьтесь с описанием отдельных сообщений, чтобы определить, должна ли эта процедура работать с ними.</span><span class="sxs-lookup"><span data-stu-id="ef342-120">Consult the descriptions of individual messages to determine whether your window procedure should handle them.</span></span>

<span data-ttu-id="ef342-121">Приложение может вызвать функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в процессе обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef342-121">Your application can call the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as part of the processing of a message.</span></span> <span data-ttu-id="ef342-122">В этом случае приложение может изменить параметры сообщения перед передачей сообщения в **дефвиндовпрок** или продолжить обработку по умолчанию после выполнения собственных операций.</span><span class="sxs-lookup"><span data-stu-id="ef342-122">In such a case, the application can modify the message parameters before passing the message to **DefWindowProc**, or it can continue with the default processing after performing its own operations.</span></span>

<span data-ttu-id="ef342-123">Процедура диалогового окна получает сообщение [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) вместо сообщения [**WM \_ CREATE**](wm-create.md) и не передает необработанные сообщения в функцию [**дефдлгпрок**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="ef342-123">A dialog box procedure receives a [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message instead of a [**WM\_CREATE**](wm-create.md) message and does not pass unprocessed messages to the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="ef342-124">В противном случае процедура диалогового окна совпадает с процедурой окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-124">Otherwise, a dialog box procedure is exactly the same as a window procedure.</span></span>

## <a name="associating-a-window-procedure-with-a-window-class"></a><span data-ttu-id="ef342-125">Связывание оконной процедуры с классом окна</span><span class="sxs-lookup"><span data-stu-id="ef342-125">Associating a Window Procedure with a Window Class</span></span>

<span data-ttu-id="ef342-126">Вы связываете процедуру окна с классом окна при регистрации класса.</span><span class="sxs-lookup"><span data-stu-id="ef342-126">You associate a window procedure with a window class when registering the class.</span></span> <span data-ttu-id="ef342-127">Необходимо заполнить структуру [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) данными о классе, а член **лпфнвндпрок** должен указывать адрес процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-127">You must fill a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure with information about the class, and the **lpfnWndProc** member must specify the address of the window procedure.</span></span> <span data-ttu-id="ef342-128">Чтобы зарегистрировать класс, передайте в функцию [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) адрес структуры **вндкласс** .</span><span class="sxs-lookup"><span data-stu-id="ef342-128">To register the class, pass the address of **WNDCLASS** structure to the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="ef342-129">После регистрации класса окна процедура окна автоматически связывается с каждым новым окном, созданным с помощью этого класса.</span><span class="sxs-lookup"><span data-stu-id="ef342-129">After the window class has been registered, the window procedure is automatically associated with each new window created with that class.</span></span>

<span data-ttu-id="ef342-130">В следующем примере показано, как связать процедуру окна в предыдущем примере с классом окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-130">The following example shows how to associate the window procedure in the previous example with a window class.</span></span>


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a><span data-ttu-id="ef342-131">Подклассировать окно</span><span class="sxs-lookup"><span data-stu-id="ef342-131">Subclassing a Window</span></span>

<span data-ttu-id="ef342-132">Чтобы создать подкласс экземпляра окна, вызовите функцию [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) и укажите в окне маркер, чтобы создать подкласс \_ флага ГВЛ WndProc и указатель на процедуру-подкласс.</span><span class="sxs-lookup"><span data-stu-id="ef342-132">To subclass an instance of a window, call the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function and specify the handle to the window to subclass the GWL\_WNDPROC flag and a pointer to the subclass procedure.</span></span> <span data-ttu-id="ef342-133">**SetWindowLong** возвращает указатель на исходную процедуру окна; Используйте этот указатель для передачи сообщений в исходную процедуру.</span><span class="sxs-lookup"><span data-stu-id="ef342-133">**SetWindowLong** returns a pointer to the original window procedure; use this pointer to pass messages to the original procedure.</span></span> <span data-ttu-id="ef342-134">Процедура окна подкласса должна использовать функцию [**каллвиндовпрок**](/windows/win32/api/winuser/nf-winuser-callwindowproca) для вызова исходной процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="ef342-134">The subclass window procedure must use the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function to call the original window procedure.</span></span>

> [!Note]  
> <span data-ttu-id="ef342-135">Чтобы написать код, совместимый как с 32-разрядными, так и с 64-разрядными версиями Windows, используйте функцию [**сетвиндовлонгптр**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .</span><span class="sxs-lookup"><span data-stu-id="ef342-135">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function.</span></span>

 

<span data-ttu-id="ef342-136">В следующем примере показано, как создать подкласс экземпляра элемента управления "поле ввода" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ef342-136">The following example shows how to subclass an instance of an edit control in a dialog box.</span></span> <span data-ttu-id="ef342-137">Процедура окна подкласса позволяет элементу управления "поле ввода" получать все вводы с клавиатуры, включая клавиши ENTER и TAB, когда элемент управления имеет фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="ef342-137">The subclass window procedure enables the edit control to receive all keyboard input, including the ENTER and TAB keys, whenever the control has the input focus.</span></span>


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
