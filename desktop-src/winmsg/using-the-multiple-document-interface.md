---
description: В этом разделе объясняется, как выполнять задачи, связанные с интерфейсом нескольких документов.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Использование интерфейса нескольких документов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656685"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="c6615-103">Использование интерфейса нескольких документов</span><span class="sxs-lookup"><span data-stu-id="c6615-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="c6615-104">В этом разделе описывается выполнение следующих задач.</span><span class="sxs-lookup"><span data-stu-id="c6615-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="c6615-105">Регистрация дочерних классов и окон фрейма</span><span class="sxs-lookup"><span data-stu-id="c6615-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="c6615-106">Создание фрейма и дочерних окон</span><span class="sxs-lookup"><span data-stu-id="c6615-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="c6615-107">Написание основного цикла сообщений</span><span class="sxs-lookup"><span data-stu-id="c6615-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="c6615-108">Написание процедуры окна фрейма</span><span class="sxs-lookup"><span data-stu-id="c6615-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="c6615-109">Написание процедуры дочернего окна</span><span class="sxs-lookup"><span data-stu-id="c6615-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="c6615-110">Создание дочернего окна</span><span class="sxs-lookup"><span data-stu-id="c6615-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="c6615-111">Чтобы проиллюстрировать эти задачи, в этом разделе содержатся примеры из Мултипад, типичного приложения многодокументного интерфейса (MDI).</span><span class="sxs-lookup"><span data-stu-id="c6615-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="c6615-112">Регистрация дочерних классов и окон фрейма</span><span class="sxs-lookup"><span data-stu-id="c6615-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="c6615-113">Обычное приложение MDI должно зарегистрировать два класса окон: одно для окна фрейма и одно для его дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="c6615-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="c6615-114">Если приложение поддерживает несколько типов документов (например, электронную таблицу и диаграмму), оно должно зарегистрировать класс окна для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="c6615-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="c6615-115">Структура класса для фрейма окна аналогична структуре класса для главного окна в приложениях, не являющихся приложениями MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="c6615-116">Структура класса для дочерних окон MDI немного отличается от структуры дочерних окон в приложениях, отличных от MDI, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c6615-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="c6615-117">Структура класса должна иметь значок, так как пользователь может максимально ограничить дочернее окно MDI так, как будто оно было обычным окном приложения.</span><span class="sxs-lookup"><span data-stu-id="c6615-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="c6615-118">Имя меню должно быть **равно NULL**, так как дочернее окно MDI не может иметь собственное меню.</span><span class="sxs-lookup"><span data-stu-id="c6615-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="c6615-119">Структура класса должна резервировать дополнительное пространство в структуре окна.</span><span class="sxs-lookup"><span data-stu-id="c6615-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="c6615-120">С помощью этого пространства приложение может связывать данные, например имя файла, с конкретным дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="c6615-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="c6615-121">В следующем примере показано, как Мултипад регистрирует свои фреймы и дочерние классы окон.</span><span class="sxs-lookup"><span data-stu-id="c6615-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="c6615-122">Создание фрейма и дочерних окон</span><span class="sxs-lookup"><span data-stu-id="c6615-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="c6615-123">После регистрации классов окон приложение MDI может создать его окна.</span><span class="sxs-lookup"><span data-stu-id="c6615-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="c6615-124">Сначала он создает окно фрейма с помощью функции [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="c6615-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="c6615-125">После создания окна фрейма приложение создает его клиентское окно с помощью **CreateWindow** или **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="c6615-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="c6615-126">Приложение должно указывать МДИКЛИЕНТ в качестве имени класса клиентского окна; **Мдиклиент** — это предварительно зарегистрированный класс окна, определенный системой.</span><span class="sxs-lookup"><span data-stu-id="c6615-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="c6615-127">Параметр *Лпвпарам* **CreateWindow** или **CreateWindowEx** должен указывать на структуру [**клиенткреатеструкт**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) .</span><span class="sxs-lookup"><span data-stu-id="c6615-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="c6615-128">Эта структура содержит элементы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c6615-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="c6615-129">Член</span><span class="sxs-lookup"><span data-stu-id="c6615-129">Member</span></span>           | <span data-ttu-id="c6615-130">Описание</span><span class="sxs-lookup"><span data-stu-id="c6615-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6615-131">**хвиндовмену**</span><span class="sxs-lookup"><span data-stu-id="c6615-131">**hWindowMenu**</span></span>  | <span data-ttu-id="c6615-132">Обработано меню окон, используемое для управления дочерними окнами MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="c6615-133">После создания дочерних окон приложение добавляет свои заголовки в меню окно в виде пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="c6615-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="c6615-134">Пользователь может активировать дочернее окно, щелкнув его заголовок в меню окно.</span><span class="sxs-lookup"><span data-stu-id="c6615-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="c6615-135">**идфирстчилд**</span><span class="sxs-lookup"><span data-stu-id="c6615-135">**idFirstChild**</span></span> | <span data-ttu-id="c6615-136">Задает идентификатор первого дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="c6615-137">Этому идентификатору назначается Первое созданное дочернее окно MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="c6615-138">Дополнительные окна создаются с увеличивающимися идентификаторами окон.</span><span class="sxs-lookup"><span data-stu-id="c6615-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="c6615-139">При уничтожении дочернего окна система немедленно переназначит идентификаторы окон, чтобы они оставались непрерывными.</span><span class="sxs-lookup"><span data-stu-id="c6615-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="c6615-140">Когда в меню окно добавляется заголовок дочернего окна, система присваивает идентификатор дочернему окну.</span><span class="sxs-lookup"><span data-stu-id="c6615-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="c6615-141">Когда пользователь щелкает заголовок дочернего окна, окно фрейма получает сообщение [**\_ команды WM**](../menurc/wm-command.md) с идентификатором в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c6615-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="c6615-142">Необходимо указать значение для элемента **идфирстчилд** , который не конфликтует с идентификаторами элементов меню в меню окна фрейма.</span><span class="sxs-lookup"><span data-stu-id="c6615-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="c6615-143">Процедура окна фрейма мултипад создает клиентское окно MDI при обработке сообщения [**о \_ создании WM**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="c6615-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="c6615-144">В следующем примере показано, как создается клиентское окно.</span><span class="sxs-lookup"><span data-stu-id="c6615-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="c6615-145">Названия дочерних окон добавляются в нижнюю часть меню окно.</span><span class="sxs-lookup"><span data-stu-id="c6615-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="c6615-146">Если приложение добавляет строки в меню окно с помощью функции [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua) , эти строки могут быть перезаписаны заголовками дочерних окон при перерисовки меню окна (при создании или уничтожении дочернего окна).</span><span class="sxs-lookup"><span data-stu-id="c6615-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="c6615-147">Приложение MDI, добавляющее строки в меню окна, должно использовать функцию [**инсертмену**](/windows/win32/api/winuser/nf-winuser-insertmenua) и проверять, что заголовки дочерних окон не переписаны эти новые строки.</span><span class="sxs-lookup"><span data-stu-id="c6615-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="c6615-148">Используйте стиль **WS \_ клипчилдрен** , чтобы создать окно клиента MDI, чтобы предотвратить Рисование окна поверх его дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="c6615-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="c6615-149">Написание основного цикла сообщений</span><span class="sxs-lookup"><span data-stu-id="c6615-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="c6615-150">Основной цикл обработки сообщений приложения MDI аналогичен сочетанию клавиш для работы с ускорителями, которые не обрабатываются в приложении MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="c6615-151">Разница заключается в том, что цикл обработки сообщений MDI вызывает функцию [**транслатемдисисакцел**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) перед проверкой для определенных приложением сочетаний клавиш или перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="c6615-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="c6615-152">В следующем примере показан цикл обработки сообщений типичного приложения MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="c6615-153">Обратите внимание, что при возникновении ошибки во внешнем [**сообщении**](/windows/win32/api/winuser/nf-winuser-getmessage) может возвращаться значение-1.</span><span class="sxs-lookup"><span data-stu-id="c6615-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="c6615-154">Функция [**транслатемдисисакцел**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) преобразует сообщения [**WM \_ KeyDown**](../inputdev/wm-keydown.md) в сообщения [**WM \_ сискомманд**](../menurc/wm-syscommand.md) и ОТПРАВЛЯЕТ их в активное дочернее окно MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="c6615-155">Если сообщение не является сообщением ускорителя MDI, функция возвращает **значение false**, в этом случае приложение использует функцию [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) , чтобы определить, были ли нажаты какие-либо из определенных приложением сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="c6615-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="c6615-156">Если нет, цикл отправляет сообщение в соответствующую процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="c6615-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="c6615-157">Написание процедуры окна фрейма</span><span class="sxs-lookup"><span data-stu-id="c6615-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="c6615-158">Оконная процедура окна фрейма MDI похожа на окно главного окна приложения, не являющегося окном MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="c6615-159">Разница заключается в том, что процедура окна фрейма передает все сообщения, которые она не обрабатывает, в функцию [**деффрамепрок**](/windows/win32/api/winuser/nf-winuser-defframeproca) , а не на функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="c6615-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="c6615-160">Кроме того, процедура окна фрейма также должна передавать некоторые сообщения, которые она обрабатывает, в том числе перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c6615-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="c6615-161">Сообщение</span><span class="sxs-lookup"><span data-stu-id="c6615-161">Message</span></span>                                  | <span data-ttu-id="c6615-162">Ответ</span><span class="sxs-lookup"><span data-stu-id="c6615-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6615-163">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="c6615-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="c6615-164">Активирует дочернее окно MDI, выбранное пользователем.</span><span class="sxs-lookup"><span data-stu-id="c6615-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="c6615-165">Это сообщение отправляется, когда пользователь выбирает дочернее окно MDI в меню окно окна фрейма MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="c6615-166">Идентификатор окна, сопровождающего это сообщение, определяет дочернее окно MDI, которое должно быть активировано.</span><span class="sxs-lookup"><span data-stu-id="c6615-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="c6615-167">**WM \_ менучар**</span><span class="sxs-lookup"><span data-stu-id="c6615-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="c6615-168">Открывает меню окно активного дочернего окна MDI, когда пользователь нажимает сочетание клавиш ALT + – (минус).</span><span class="sxs-lookup"><span data-stu-id="c6615-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="c6615-169">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="c6615-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="c6615-170">Передает фокус клавиатуры окну клиента MDI, которое, в свою очередь, передает его в активное дочернее окно MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="c6615-171">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="c6615-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="c6615-172">Изменяет размер окна клиента MDI, чтобы оно поместилось в клиентскую область окна нового фрейма.</span><span class="sxs-lookup"><span data-stu-id="c6615-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="c6615-173">Если процедура окна фрейма изменяет размер окна клиента MDI на другой, он не должен передавать сообщение в функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="c6615-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="c6615-174">Процедура окна фрейма в Мултипад называется Мпфрамевндпрок.</span><span class="sxs-lookup"><span data-stu-id="c6615-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="c6615-175">Обработка других сообщений с помощью Мпфрамевндпрок аналогична обработке приложений, не относящихся к MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="c6615-176">[**WM \_ КОМАНДные**](../menurc/wm-command.md) сообщения в мултипад обрабатываются локально определенной функцией коммандхандлер.</span><span class="sxs-lookup"><span data-stu-id="c6615-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="c6615-177">Для командных сообщений Мултипад не обрабатывается, Коммандхандлер вызывает функцию [**деффрамепрок**](/windows/win32/api/winuser/nf-winuser-defframeproca) .</span><span class="sxs-lookup"><span data-stu-id="c6615-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="c6615-178">Если Мултипад не использует **деффрамепрок** по умолчанию, пользователь не сможет активировать дочернее окно из меню окно, так как **сообщение \_ команды WM** , отправленное щелчком пункта меню окна, будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="c6615-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="c6615-179">Написание процедуры дочернего окна</span><span class="sxs-lookup"><span data-stu-id="c6615-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="c6615-180">Как и процедура окна фрейма, процедура дочернего окна MDI использует специальную функцию для обработки сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6615-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="c6615-181">Все сообщения, не обрабатываемые процедурой дочернего окна, должны передаваться в функцию [**дефмдичилдпрок**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) , а не в функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="c6615-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="c6615-182">Кроме того, некоторые сообщения управления окнами должны передаваться в **дефмдичилдпрок**, даже если приложение обрабатывает сообщение, чтобы интерфейс MDI правильно функционировал.</span><span class="sxs-lookup"><span data-stu-id="c6615-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="c6615-183">Ниже приведены сообщения, которые приложение должно передать в **дефмдичилдпрок**.</span><span class="sxs-lookup"><span data-stu-id="c6615-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="c6615-184">Сообщение</span><span class="sxs-lookup"><span data-stu-id="c6615-184">Message</span></span>                                       | <span data-ttu-id="c6615-185">Ответ</span><span class="sxs-lookup"><span data-stu-id="c6615-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6615-186">**WM \_ чилдактивате**</span><span class="sxs-lookup"><span data-stu-id="c6615-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="c6615-187">Выполняет обработку активации при изменении размера, перемещении или отображении дочерних окон MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="c6615-188">Это сообщение должно быть передано.</span><span class="sxs-lookup"><span data-stu-id="c6615-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="c6615-189">**WM \_ жетминмаксинфо**</span><span class="sxs-lookup"><span data-stu-id="c6615-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="c6615-190">Вычисляет размер развернутого дочернего окна MDI на основе текущего размера окна клиента MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="c6615-191">**WM \_ менучар**</span><span class="sxs-lookup"><span data-stu-id="c6615-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="c6615-192">Передает сообщение в окно фрейма MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="c6615-193">**\_Перемещение WM**</span><span class="sxs-lookup"><span data-stu-id="c6615-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="c6615-194">Повторно вычисляет полосы прокрутки клиента MDI, если они есть.</span><span class="sxs-lookup"><span data-stu-id="c6615-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="c6615-195">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="c6615-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="c6615-196">Активирует дочернее окно, если оно не является активным дочерним окном MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c6615-197">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="c6615-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="c6615-198">Выполняет операции, необходимые для изменения размера окна, особенно для максимизации или восстановления дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="c6615-199">Сбой передачи этого сообщения функции [**дефмдичилдпрок**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) дает очень нежелательные результаты.</span><span class="sxs-lookup"><span data-stu-id="c6615-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="c6615-200">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="c6615-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="c6615-201">Обрабатывает команды меню окна (ранее известные как системные): **SC \_ некствиндов**, **SC \_ преввиндов**, **SC \_ Move**, **SC \_ size** и **SC \_**.</span><span class="sxs-lookup"><span data-stu-id="c6615-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="c6615-202">Создание дочернего окна</span><span class="sxs-lookup"><span data-stu-id="c6615-202">Creating a Child Window</span></span>

<span data-ttu-id="c6615-203">Чтобы создать дочернее окно MDI, приложение может либо вызвать функцию [**креатемдивиндов**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) , либо отправить сообщение [**\_ мдикреате WM**](wm-mdicreate.md) в окно клиента MDI.</span><span class="sxs-lookup"><span data-stu-id="c6615-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="c6615-204">(Приложение может использовать функцию [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) с стилем **WS \_ ex \_ МДИЧИЛД** для создания дочерних окон MDI.) Однопотоковое приложение MDI может использовать любой из этих методов для создания дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="c6615-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="c6615-205">Поток в многопоточном приложении MDI должен использовать функцию **креатемдивиндов** или **CreateWindowEx** для создания дочернего окна в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="c6615-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="c6615-206">Параметр *lParam* сообщения [**WM \_ мдикреате**](wm-mdicreate.md) является дальней указателем на структуру [**мдикреатеструкт**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="c6615-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="c6615-207">Структура включает четыре элемента измерения: **x** и **y**, которые указывают горизонтальное и вертикальное положение окна, а также **CX** и **CY**, которые указывают горизонтальные и вертикальные экстенты окна.</span><span class="sxs-lookup"><span data-stu-id="c6615-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="c6615-208">Любой из этих членов может быть явно назначен приложением или для них может быть задано значение **\_ Уседефаулт во Вт**. в этом случае система выбирает в соответствии с каскадным алгоритмом расположение, размер или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="c6615-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="c6615-209">В любом случае необходимо инициализировать все четыре члена.</span><span class="sxs-lookup"><span data-stu-id="c6615-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="c6615-210">Для всех измерений мултипад использует **\_ Уседефаулт во Вт** .</span><span class="sxs-lookup"><span data-stu-id="c6615-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="c6615-211">Последним элементом структуры [**мдикреатеструкт**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) является элемент **Style** , который может содержать биты стиля для окна.</span><span class="sxs-lookup"><span data-stu-id="c6615-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="c6615-212">Чтобы создать дочернее окно MDI, которое может иметь любое сочетание стилей окна, укажите стиль окна **мдис \_ аллчилдстилес** .</span><span class="sxs-lookup"><span data-stu-id="c6615-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="c6615-213">Если этот стиль не указан, дочернее окно MDI имеет стили **WS \_ Minimize**, **WS \_ максимизации**, **WS \_ HSCROLL** и **WS \_ VSCROLL** в качестве параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6615-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="c6615-214">Мултипад создает дочерние окна MDI, используя локально определенную функцию AddFile (расположенную в исходном файле МПФИЛЕ. C).</span><span class="sxs-lookup"><span data-stu-id="c6615-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="c6615-215">Функция AddFile задает заголовок дочернего окна, присваивая элементу **сзтитле** структуры [**мдикреатеструкт**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) окна либо имя редактируемого файла, либо "без названия".</span><span class="sxs-lookup"><span data-stu-id="c6615-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="c6615-216">Элементу **сзкласс** присваивается имя класса дочернего окна MDI, зарегистрированное в функции инитиализеаппликатион мултипад.</span><span class="sxs-lookup"><span data-stu-id="c6615-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="c6615-217">Для элемента **ховнер** задается экземпляр приложения.</span><span class="sxs-lookup"><span data-stu-id="c6615-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="c6615-218">В следующем примере показана функция AddFile в Мултипад.</span><span class="sxs-lookup"><span data-stu-id="c6615-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="c6615-219">Указатель, переданный в параметре *lParam* сообщения [**WM \_ мдикреате**](wm-mdicreate.md) , передается в функцию [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) и отображается как первый элемент в структуре [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , переданный в сообщении [**WM \_ CREATE**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="c6615-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="c6615-220">В Мултипад дочернее окно инициализируется автоматически во время обработки сообщений обработчиком **WM \_** , путем инициализации переменных документа в дополнительных данных и создания дочернего окна редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c6615-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
