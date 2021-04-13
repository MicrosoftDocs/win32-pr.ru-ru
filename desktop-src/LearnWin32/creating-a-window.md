---
title: Создание окна
description: .
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126f040d72fec423ad5b6f3ecb31bc780a3192b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412974"
---
# <a name="creating-a-window"></a><span data-ttu-id="973c4-103">Создание окна</span><span class="sxs-lookup"><span data-stu-id="973c4-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="973c4-104">Классы окон</span><span class="sxs-lookup"><span data-stu-id="973c4-104">Window Classes</span></span>

<span data-ttu-id="973c4-105">*Класс окна* определяет набор поведений, которые могут встречаться в нескольких окнах.</span><span class="sxs-lookup"><span data-stu-id="973c4-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="973c4-106">Например, в группе кнопок каждая кнопка имеет аналогичное поведение, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="973c4-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="973c4-107">Конечно, кнопки не полностью идентичны; Каждая кнопка отображает собственную текстовую строку и имеет собственные экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="973c4-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="973c4-108">Данные, уникальные для каждого окна, называются *данными экземпляра*.</span><span class="sxs-lookup"><span data-stu-id="973c4-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="973c4-109">Каждое окно должно быть связано с классом окна, даже если программа создает только один экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="973c4-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="973c4-110">Важно понимать, что класс окна не является "классом" в смысле C++.</span><span class="sxs-lookup"><span data-stu-id="973c4-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="973c4-111">Вместо этого это структура данных, используемая внутри операционной системы.</span><span class="sxs-lookup"><span data-stu-id="973c4-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="973c4-112">Классы окон регистрируются в системе во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="973c4-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="973c4-113">Чтобы зарегистрировать новый класс окна, начните с заполнения структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) :</span><span class="sxs-lookup"><span data-stu-id="973c4-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="973c4-114">Необходимо задать следующие члены структуры:</span><span class="sxs-lookup"><span data-stu-id="973c4-114">You must set the following structure members:</span></span>

- <span data-ttu-id="973c4-115">**лпфнвндпрок** — это указатель на определяемую приложением функцию, называемую *процедурой окна* или «процедурой окна».</span><span class="sxs-lookup"><span data-stu-id="973c4-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="973c4-116">Процедура окна определяет большую часть поведения окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="973c4-117">Далее мы рассмотрим процедуру Windows.</span><span class="sxs-lookup"><span data-stu-id="973c4-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="973c4-118">Сейчас просто рассматривайте это как прямую ссылку.</span><span class="sxs-lookup"><span data-stu-id="973c4-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="973c4-119">**HINSTANCE** — это обработчик экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="973c4-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="973c4-120">Получите это значение из параметра *HINSTANCE* объекта **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="973c4-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="973c4-121">**лпсзкласснаме** — это строка, идентифицирующая класс окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="973c4-122">Имена классов являются локальными для текущего процесса, поэтому имя должно быть уникальным только в пределах процесса.</span><span class="sxs-lookup"><span data-stu-id="973c4-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="973c4-123">Однако стандартные элементы управления Windows также имеют классы.</span><span class="sxs-lookup"><span data-stu-id="973c4-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="973c4-124">При использовании любого из этих элементов управления необходимо выбрать имена классов, которые не конфликтуют с именами классов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="973c4-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="973c4-125">Например, класс окна для элемента управления Button называется "Button".</span><span class="sxs-lookup"><span data-stu-id="973c4-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="973c4-126">Структура [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) содержит другие элементы, не показанные здесь.</span><span class="sxs-lookup"><span data-stu-id="973c4-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="973c4-127">Можно задать для них нулевое значение, как показано в этом примере, или заполнить их в.</span><span class="sxs-lookup"><span data-stu-id="973c4-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="973c4-128">Эта структура подробно описана в документации MSDN.</span><span class="sxs-lookup"><span data-stu-id="973c4-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="973c4-129">Затем передайте адрес структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) в функцию [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="973c4-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="973c4-130">Эта функция регистрирует класс окна в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="973c4-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="973c4-131">Создание окна</span><span class="sxs-lookup"><span data-stu-id="973c4-131">Creating the Window</span></span>

<span data-ttu-id="973c4-132">Чтобы создать новый экземпляр окна, вызовите функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) :</span><span class="sxs-lookup"><span data-stu-id="973c4-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
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
```

<span data-ttu-id="973c4-133">Вы можете ознакомиться с подробными описаниями параметров в MSDN, но вот краткий обзор:</span><span class="sxs-lookup"><span data-stu-id="973c4-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="973c4-134">Первый параметр позволяет указать некоторые необязательные поведения для окна (например, прозрачные окна).</span><span class="sxs-lookup"><span data-stu-id="973c4-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="973c4-135">Присвойте этому параметру значение 0 для поведения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="973c4-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="973c4-136">`CLASS_NAME` имя класса окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="973c4-137">Определяет тип создаваемого окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="973c4-138">Текст окна используется различными способами для различных типов окон.</span><span class="sxs-lookup"><span data-stu-id="973c4-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="973c4-139">Если окно содержит заголовок, текст отображается в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="973c4-140">Стиль окна — это набор флагов, определяющих некоторый вид окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="973c4-141">Константа **WS \_ оверлаппедвиндов** фактически является несколько флагов в сочетании с побитовой **или**.</span><span class="sxs-lookup"><span data-stu-id="973c4-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="973c4-142">Вместе эти флаги предоставляют окну строку заголовка, границу, системное меню, а также кнопки **сворачивания** и **развертывания** .</span><span class="sxs-lookup"><span data-stu-id="973c4-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="973c4-143">Этот набор флагов является наиболее распространенным стилем для окна приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="973c4-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="973c4-144">Для расположения и размера константа **во вт. \_ уседефаулт** означает использование значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="973c4-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="973c4-145">Следующий параметр задает родительское окно или окно-владелец для нового окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="973c4-146">Если вы создаете дочернее окно, задайте родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="973c4-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="973c4-147">Для окна верхнего уровня задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="973c4-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="973c4-148">Для окна приложения следующий параметр определяет меню для окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="973c4-149">В этом примере не используется меню, поэтому значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="973c4-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="973c4-150">*HINSTANCE* — это обработчик экземпляра, описанный выше.</span><span class="sxs-lookup"><span data-stu-id="973c4-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="973c4-151">(См. статью [WinMain: точка входа приложения](winmain--the-application-entry-point.md).)</span><span class="sxs-lookup"><span data-stu-id="973c4-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="973c4-152">Последний параметр является указателем на произвольные данные типа **void \***.</span><span class="sxs-lookup"><span data-stu-id="973c4-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="973c4-153">Это значение можно использовать для передачи структуры данных в оконную процедуру.</span><span class="sxs-lookup"><span data-stu-id="973c4-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="973c4-154">Мы покажем один из возможных способов использования этого параметра в разделе [Управление состоянием приложения](managing-application-state-.md).</span><span class="sxs-lookup"><span data-stu-id="973c4-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="973c4-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) возвращает маркер в новое окно или нуль, если функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="973c4-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="973c4-156">Чтобы отобразить окно, т. е. сделать окно видимым, передайте в функцию [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) маркер окна:</span><span class="sxs-lookup"><span data-stu-id="973c4-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="973c4-157">Параметр *HWND* — это дескриптор окна, возвращаемый функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="973c4-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="973c4-158">Параметр *нкмдшов* можно использовать для сворачивания или разворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="973c4-159">Операционная система передает это значение в программу с помощью функции **wWinMain** .</span><span class="sxs-lookup"><span data-stu-id="973c4-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="973c4-160">Ниже приведен полный код для создания окна.</span><span class="sxs-lookup"><span data-stu-id="973c4-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="973c4-161">Помните, что `WindowProc` все еще является прямым объявлением функции.</span><span class="sxs-lookup"><span data-stu-id="973c4-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
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
```

<span data-ttu-id="973c4-162">Поздравляем, вы создали окно!</span><span class="sxs-lookup"><span data-stu-id="973c4-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="973c4-163">Сейчас окно не содержит никакого содержимого или взаимодействует с пользователем.</span><span class="sxs-lookup"><span data-stu-id="973c4-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="973c4-164">В реальном приложении GUI окно будет реагировать на события пользователя и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="973c4-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="973c4-165">В следующем разделе описывается, как сообщения в окне предоставляют такую сортировку.</span><span class="sxs-lookup"><span data-stu-id="973c4-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="973c4-166">Следующая</span><span class="sxs-lookup"><span data-stu-id="973c4-166">Next</span></span>

[<span data-ttu-id="973c4-167">Сообщения окна</span><span class="sxs-lookup"><span data-stu-id="973c4-167">Window Messages</span></span>](window-messages.md)