---
description: В примерах этого раздела описывается выполнение задач, связанных с использованием Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Использование Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912607"
---
# <a name="using-windows"></a><span data-ttu-id="67f81-103">Использование Windows</span><span class="sxs-lookup"><span data-stu-id="67f81-103">Using Windows</span></span>

<span data-ttu-id="67f81-104">В примерах этого раздела описывается выполнение следующих задач.</span><span class="sxs-lookup"><span data-stu-id="67f81-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="67f81-105">Создание главного окна</span><span class="sxs-lookup"><span data-stu-id="67f81-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="67f81-106">Создание, перечисление и изменение размеров дочерних окон</span><span class="sxs-lookup"><span data-stu-id="67f81-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="67f81-107">Уничтожение окна</span><span class="sxs-lookup"><span data-stu-id="67f81-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="67f81-108">Использование многоуровневых окон</span><span class="sxs-lookup"><span data-stu-id="67f81-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="67f81-109">Создание главного окна</span><span class="sxs-lookup"><span data-stu-id="67f81-109">Creating a Main Window</span></span>

<span data-ttu-id="67f81-110">Первое окно, создаваемое приложением, обычно является главным окном.</span><span class="sxs-lookup"><span data-stu-id="67f81-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="67f81-111">Главное окно создается с помощью функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) с указанием класса окна, имени окна, стилей окна, размера, расположения, маркера меню, маркера экземпляра и данных для создания.</span><span class="sxs-lookup"><span data-stu-id="67f81-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="67f81-112">Главное окно относится к классу окон, определяемому приложением, поэтому необходимо зарегистрировать класс окна и предоставить оконную процедуру для класса перед созданием главного окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="67f81-113">Большинство приложений обычно используют стиль [**WS \_ оверлаппедвиндов**](window-styles.md) для создания главного окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="67f81-114">Этот стиль дает окну строку заголовка, меню окна, границу изменения размера, а также кнопки сворачивания и развертывания.</span><span class="sxs-lookup"><span data-stu-id="67f81-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="67f81-115">Функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) возвращает маркер, который однозначно идентифицирует окно.</span><span class="sxs-lookup"><span data-stu-id="67f81-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="67f81-116">В следующем примере создается главное окно, принадлежащее классу окна, определяемому приложением.</span><span class="sxs-lookup"><span data-stu-id="67f81-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="67f81-117">Имя окна, **главное окно**, появится в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="67f81-118">Комбинируя стили [**WS \_ VSCROLL**](window-styles.md) и **WS \_ HSCROLL** с стилем **WS \_ оверлаппедвиндов** , приложение создает главное окно с горизонтальной и вертикальной полосами прокрутки в дополнение к компонентам, предоставляемым стилем **WS \_ оверлаппедвиндов** .</span><span class="sxs-lookup"><span data-stu-id="67f81-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="67f81-119">Четыре вхождения константы **\_ Уседефаулт во Вт** . устанавливают исходный размер и расположение окна в значения по умолчанию, определяемые системой.</span><span class="sxs-lookup"><span data-stu-id="67f81-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="67f81-120">При указании **значения NULL** вместо маркера меню окно будет иметь меню, определенное для класса Window.</span><span class="sxs-lookup"><span data-stu-id="67f81-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



<span data-ttu-id="67f81-121">Обратите внимание, что в предыдущем примере функция [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) вызывается после создания главного окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="67f81-122">Это делается потому, что система не отображает автоматически главное окно после его создания.</span><span class="sxs-lookup"><span data-stu-id="67f81-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="67f81-123">Передавая флаг **SW \_ Шовдефаулт** в **ShowWindow**, приложение позволяет программе, запустившего приложение, установить начальное состояние отображения главного окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="67f81-124">Функция [**упдатевиндов**](/windows/win32/api/winuser/nf-winuser-updatewindow) отправляет окну свое первое сообщение [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="67f81-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="67f81-125">Создание, перечисление и изменение размеров дочерних окон</span><span class="sxs-lookup"><span data-stu-id="67f81-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="67f81-126">Вы можете разделить клиентскую область окна на разные функциональные области с помощью дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="67f81-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="67f81-127">Создание дочернего окна похоже на создание главного окна — используется функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="67f81-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="67f81-128">Чтобы создать окно класса, определяемого приложением, необходимо зарегистрировать класс окна и предоставить процедуру окна перед созданием дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="67f81-129">Необходимо предоставить дочернему окну стиль дочернего окна [**WS \_**](window-styles.md) и указать родительское окно для дочернего окна при его создании.</span><span class="sxs-lookup"><span data-stu-id="67f81-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="67f81-130">В следующем примере клиентская область главного окна приложения делится на три функциональные области путем создания трех дочерних окон одинакового размера.</span><span class="sxs-lookup"><span data-stu-id="67f81-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="67f81-131">Каждое дочернее окно имеет ту же высоту, что и клиентскую область главного окна, но каждая из них имеет одну треть ее ширину.</span><span class="sxs-lookup"><span data-stu-id="67f81-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="67f81-132">Главное окно создает дочерние окна в ответ на сообщение [**о \_ создании WM**](wm-create.md) , которое основное окно получает в процессе создания окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="67f81-133">Так как у каждого дочернего окна есть стиль [**\_ границы WS**](window-styles.md) , у каждого из них есть тонкая граница.</span><span class="sxs-lookup"><span data-stu-id="67f81-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="67f81-134">Кроме того, поскольку стиль " **WS \_ Visible** " не указан, каждое дочернее окно изначально скрыто.</span><span class="sxs-lookup"><span data-stu-id="67f81-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="67f81-135">Кроме того, обратите внимание, что каждому дочернему окну назначается идентификатор дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="67f81-136">Основное окно изменяет размеры и положение дочерних окон в ответ на сообщение о [**\_ размере WM**](wm-size.md) , которое основное окно получает при изменении его размера.</span><span class="sxs-lookup"><span data-stu-id="67f81-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="67f81-137">В ответ на **\_ изменение размера WM** главное окно получает размеры клиентской области с помощью функции [**жетклиентрект**](/windows/win32/api/winuser/nf-winuser-getclientrect) , а затем передает измерения в функцию [**енумчилдвиндовс**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) .</span><span class="sxs-lookup"><span data-stu-id="67f81-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="67f81-138">**Енумчилдвиндовс** передает этот обработчик в каждое дочернее окно, в свою очередь, в функцию обратного вызова [**енумчилдпрок**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) , определяемую приложением.</span><span class="sxs-lookup"><span data-stu-id="67f81-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="67f81-139">Эта функция изменяет размеры и положение каждого дочернего окна, вызывая функцию [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) . Размер и расположение основаны на измерениях клиентской области главного окна и идентификаторе дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="67f81-140">После этого **енумчилдпрок** вызывает функцию [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) , чтобы сделать окно видимым.</span><span class="sxs-lookup"><span data-stu-id="67f81-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a><span data-ttu-id="67f81-141">Уничтожение окна</span><span class="sxs-lookup"><span data-stu-id="67f81-141">Destroying a Window</span></span>

<span data-ttu-id="67f81-142">Для уничтожения окна можно использовать функцию [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="67f81-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="67f81-143">Как правило, приложение отправляет сообщение [**о \_ закрытии WM**](wm-close.md) перед уничтожением окна, предоставляя ему возможность запросить подтверждение перед уничтожением окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="67f81-144">Окно, содержащее меню "окно", автоматически получает сообщение о **\_ закрытии WM** при нажатии пользователем кнопки " **Закрыть** " в меню "окно".</span><span class="sxs-lookup"><span data-stu-id="67f81-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="67f81-145">Если пользователь подтверждает, что окно должно быть уничтожено, приложение вызывает **дестройвиндов**.</span><span class="sxs-lookup"><span data-stu-id="67f81-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="67f81-146">Система отправляет сообщение [**WM \_ destroy**](wm-destroy.md) в окно после его удаления с экрана.</span><span class="sxs-lookup"><span data-stu-id="67f81-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="67f81-147">В ответ на попытку **WM \_ destroy** окно сохраняет свои данные и освобождает все выделенные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="67f81-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="67f81-148">Главное окно завершает обработку **WM \_ destroy** , вызывая функцию [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) для выхода из приложения.</span><span class="sxs-lookup"><span data-stu-id="67f81-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="67f81-149">В следующем примере показано, как запросить подтверждение пользователя перед уничтожением окна.</span><span class="sxs-lookup"><span data-stu-id="67f81-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="67f81-150">В ответ на [**запрос WM \_ Close**](wm-close.md)в примере отображается диалоговое окно, содержащее кнопки **Да**, **нет** и **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="67f81-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="67f81-151">Если пользователь нажмет кнопку **Да**, вызывается [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) . в противном случае окно не уничтожается.</span><span class="sxs-lookup"><span data-stu-id="67f81-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="67f81-152">Так как окно, которое уничтожается, является главным окном, пример вызывает [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) в ответ на функцию [**WM \_ destroy**](wm-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="67f81-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a><span data-ttu-id="67f81-153">Использование многоуровневых окон</span><span class="sxs-lookup"><span data-stu-id="67f81-153">Using Layered Windows</span></span>

<span data-ttu-id="67f81-154">Чтобы диалоговое окно поступало в виде полупрозрачного окна, сначала создайте диалоговое окно, как обычно.</span><span class="sxs-lookup"><span data-stu-id="67f81-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="67f81-155">Затем в [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md)задайте многоуровневый бит расширенного стиля окна и вызовите [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) с нужным альфа-значением.</span><span class="sxs-lookup"><span data-stu-id="67f81-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="67f81-156">Код может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="67f81-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="67f81-157">Обратите внимание, что третий параметр [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) имеет значение в диапазоне от 0 до 255, и 0 делает окно полностью прозрачным и 255 делает его полностью непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="67f81-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="67f81-158">Этот параметр имитирует более гибкую [**блендфунктион**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) функции [**алфабленд**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="67f81-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="67f81-159">Чтобы сделать это окно полностью непрозрачным, удалите **\_ \_ Многоуровневый бит WS ex** , вызвав [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , а затем запросите окно для перерисовки.</span><span class="sxs-lookup"><span data-stu-id="67f81-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="67f81-160">Удаление бита необходимо, чтобы система могла понять, что она может освободить некоторый объем памяти, связанный с разслойом и перенаправлением.</span><span class="sxs-lookup"><span data-stu-id="67f81-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="67f81-161">Код может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="67f81-161">The code might look like this:</span></span>


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



<span data-ttu-id="67f81-162">Чтобы использовать многоуровневые дочерние окна, приложение должно объявить себя в манифесте с поддержкой Windows 8.</span><span class="sxs-lookup"><span data-stu-id="67f81-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
