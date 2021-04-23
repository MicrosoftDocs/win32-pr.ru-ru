---
title: Управление состоянием приложения
description: Оконная процедура — это просто функция, которая вызывается для каждого сообщения, поэтому она по сути не имеет состояния. Поэтому необходим способ отслеживания состояния приложения от одного вызова функции к следующему.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069979"
---
# <a name="managing-application-state"></a><span data-ttu-id="db6b3-104">Управление состоянием приложения</span><span class="sxs-lookup"><span data-stu-id="db6b3-104">Managing Application State</span></span>

<span data-ttu-id="db6b3-105">Оконная процедура — это просто функция, которая вызывается для каждого сообщения, поэтому она по сути не имеет состояния.</span><span class="sxs-lookup"><span data-stu-id="db6b3-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="db6b3-106">Поэтому необходим способ отслеживания состояния приложения от одного вызова функции к следующему.</span><span class="sxs-lookup"><span data-stu-id="db6b3-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="db6b3-107">Самый простой подход — просто поместить все в глобальные переменные.</span><span class="sxs-lookup"><span data-stu-id="db6b3-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="db6b3-108">Это хорошо подходит для небольших программ, и многие из примеров пакета SDK используют этот подход.</span><span class="sxs-lookup"><span data-stu-id="db6b3-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="db6b3-109">Однако в большой программе она приводит к распространению глобальных переменных.</span><span class="sxs-lookup"><span data-stu-id="db6b3-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="db6b3-110">Кроме того, у вас может быть несколько окон, каждая из которых имеет собственную процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="db6b3-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="db6b3-111">Отслеживание того, какое окно должно иметь доступ, какие переменные становятся запутанными и подвержены ошибкам.</span><span class="sxs-lookup"><span data-stu-id="db6b3-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="db6b3-112">Функция [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) предоставляет способ передачи любой структуры данных в окно.</span><span class="sxs-lookup"><span data-stu-id="db6b3-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="db6b3-113">При вызове этой функции в оконную процедуру отправляются следующие два сообщения:</span><span class="sxs-lookup"><span data-stu-id="db6b3-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="db6b3-114">**WM \_ нккреате**</span><span class="sxs-lookup"><span data-stu-id="db6b3-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="db6b3-115">**\_Создание WM**</span><span class="sxs-lookup"><span data-stu-id="db6b3-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="db6b3-116">Эти сообщения отправляются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="db6b3-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="db6b3-117">(Они не являются единственными двумя сообщениями, отправленными во время [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), но мы можем игнорировать другие для этого обсуждения.)</span><span class="sxs-lookup"><span data-stu-id="db6b3-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="db6b3-118">Сообщение [**WM \_ Нккреате**](/windows/desktop/winmsg/wm-nccreate) и [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) отправляются до того, как окно станет видимым.</span><span class="sxs-lookup"><span data-stu-id="db6b3-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="db6b3-119">Это делает их хорошим местом для инициализации пользовательского интерфейса, например, для определения первоначального макета окна.</span><span class="sxs-lookup"><span data-stu-id="db6b3-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="db6b3-120">Последний параметр [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) является указателем типа **void \***.</span><span class="sxs-lookup"><span data-stu-id="db6b3-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="db6b3-121">В этом параметре можно передать любое значение указателя.</span><span class="sxs-lookup"><span data-stu-id="db6b3-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="db6b3-122">Когда процедура окна обрабатывает сообщение [**WM \_ Нккреате**](/windows/desktop/winmsg/wm-nccreate) или [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) , оно может извлекать это значение из данных сообщения.</span><span class="sxs-lookup"><span data-stu-id="db6b3-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="db6b3-123">Давайте посмотрим, как использовать этот параметр для передачи данных приложения в окно.</span><span class="sxs-lookup"><span data-stu-id="db6b3-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="db6b3-124">Сначала определите класс или структуру, которые содержат сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="db6b3-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="db6b3-125">При вызове [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)передайте указатель на эту структуру в последнем параметре **void \*** .</span><span class="sxs-lookup"><span data-stu-id="db6b3-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

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
    pState      // Additional application data
    );
```

<span data-ttu-id="db6b3-126">Когда вы получаете сообщения [**\_ Нккреате**](/windows/desktop/winmsg/wm-nccreate) и [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) , параметр *lParam* каждого сообщения является указателем на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="db6b3-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="db6b3-127">Структура **CREATESTRUCT** , в свою очередь, содержит указатель, переданный в [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="db6b3-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![Схема, на которой показан макет структуры CREATESTRUCT](images/appstate01.png)

<span data-ttu-id="db6b3-129">Вот как можно извлечь указатель на структуру данных.</span><span class="sxs-lookup"><span data-stu-id="db6b3-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="db6b3-130">Сначала получите структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) путем приведения параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="db6b3-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="db6b3-131">Элемент **лпкреатепарамс** структуры [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) является исходным указателем void, указанным в [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="db6b3-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="db6b3-132">Получите указатель на собственную структуру данных путем приведения **лпкреатепарамс**.</span><span class="sxs-lookup"><span data-stu-id="db6b3-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="db6b3-133">Затем вызовите функцию [**сетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) и передайте указатель в структуру данных.</span><span class="sxs-lookup"><span data-stu-id="db6b3-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="db6b3-134">Цель последнего вызова функции — сохранить указатель *статеинфо* в данных экземпляра для окна.</span><span class="sxs-lookup"><span data-stu-id="db6b3-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="db6b3-135">После этого вы всегда можете вернуть указатель из окна, вызвав [**жетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span><span class="sxs-lookup"><span data-stu-id="db6b3-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="db6b3-136">Каждое окно имеет свои данные экземпляра, поэтому можно создать несколько окон и присвоить каждому окну собственный экземпляр структуры данных.</span><span class="sxs-lookup"><span data-stu-id="db6b3-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="db6b3-137">Этот подход особенно удобен, если вы определяете класс Windows и создаете более одного окна этого класса, например, при создании пользовательского класса элемента управления.</span><span class="sxs-lookup"><span data-stu-id="db6b3-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="db6b3-138">В небольшой вспомогательной функции удобно обернуть вызов [**жетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) .</span><span class="sxs-lookup"><span data-stu-id="db6b3-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="db6b3-139">Теперь можно написать процедуру окна следующим образом.</span><span class="sxs-lookup"><span data-stu-id="db6b3-139">Now you can write your window procedure as follows.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a><span data-ttu-id="db6b3-140">Object-Orientedный подход</span><span class="sxs-lookup"><span data-stu-id="db6b3-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="db6b3-141">Этот подход можно расширить.</span><span class="sxs-lookup"><span data-stu-id="db6b3-141">We can extend this approach further.</span></span> <span data-ttu-id="db6b3-142">Мы уже определили структуру данных для хранения сведений о состоянии окна.</span><span class="sxs-lookup"><span data-stu-id="db6b3-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="db6b3-143">Имеет смысл предоставить эту структуру данных с помощью функций-членов (методов), которые работают с данными.</span><span class="sxs-lookup"><span data-stu-id="db6b3-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="db6b3-144">Это естественно ведет к проектированию, где структура (или класс) отвечает за все операции в окне.</span><span class="sxs-lookup"><span data-stu-id="db6b3-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="db6b3-145">Затем процедура окна станет частью класса.</span><span class="sxs-lookup"><span data-stu-id="db6b3-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="db6b3-146">Другими словами, мы хотели бы проделать следующее:</span><span class="sxs-lookup"><span data-stu-id="db6b3-146">In other words, we would like to go from this:</span></span>

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

<span data-ttu-id="db6b3-147">На эту:</span><span class="sxs-lookup"><span data-stu-id="db6b3-147">To this:</span></span>

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

<span data-ttu-id="db6b3-148">Единственная проблема заключается в том, как подключить `MyWindow::WindowProc` метод.</span><span class="sxs-lookup"><span data-stu-id="db6b3-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="db6b3-149">Функция [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) ждет, что процедура окна является указателем на функцию.</span><span class="sxs-lookup"><span data-stu-id="db6b3-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="db6b3-150">Нельзя передать указатель на функцию-член (не статическую) в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="db6b3-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="db6b3-151">Однако можно передать указатель на *статическую* функцию-член, а затем делегировать ее функции-члену.</span><span class="sxs-lookup"><span data-stu-id="db6b3-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="db6b3-152">Ниже приведен шаблон класса, демонстрирующий этот подход:</span><span class="sxs-lookup"><span data-stu-id="db6b3-152">Here is a class template that shows this approach:</span></span>

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

<span data-ttu-id="db6b3-153">`BaseWindow`Класс является абстрактным базовым классом, от которого наследуются определенные классы окон.</span><span class="sxs-lookup"><span data-stu-id="db6b3-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="db6b3-154">Например, ниже приведено объявление простого класса, производного от `BaseWindow` :</span><span class="sxs-lookup"><span data-stu-id="db6b3-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="db6b3-155">Чтобы создать окно, вызовите `BaseWindow::Create` :</span><span class="sxs-lookup"><span data-stu-id="db6b3-155">To create the window, call `BaseWindow::Create`:</span></span>

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

<span data-ttu-id="db6b3-156">`BaseWindow::HandleMessage`Для реализации процедуры окна используется чистый виртуальный метод.</span><span class="sxs-lookup"><span data-stu-id="db6b3-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="db6b3-157">Например, следующая реализация эквивалентна процедуре окна, показанной в начале [модуля 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="db6b3-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

<span data-ttu-id="db6b3-158">Обратите внимание, что дескриптор окна хранится в переменной-члене (*m \_ HWND*), поэтому нам не нужно передавать его в качестве параметра в `HandleMessage` .</span><span class="sxs-lookup"><span data-stu-id="db6b3-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="db6b3-159">Многие из существующих платформ программирования Windows, таких как Microsoft Foundation Classes (MFC) и библиотека ATL, используют подходы, похожие на показанные здесь.</span><span class="sxs-lookup"><span data-stu-id="db6b3-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="db6b3-160">Конечно, полностью обобщенная платформа, такая как MFC, сложнее, чем этот сравнительно простой пример.</span><span class="sxs-lookup"><span data-stu-id="db6b3-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="db6b3-161">Следующая</span><span class="sxs-lookup"><span data-stu-id="db6b3-161">Next</span></span>

[<span data-ttu-id="db6b3-162">Модуль 2. Использование COM в программе Windows</span><span class="sxs-lookup"><span data-stu-id="db6b3-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="db6b3-163">См. также</span><span class="sxs-lookup"><span data-stu-id="db6b3-163">Related topics</span></span>

[<span data-ttu-id="db6b3-164">Пример Басевиндов</span><span class="sxs-lookup"><span data-stu-id="db6b3-164">BaseWindow Sample</span></span>](basewindow-sample.md)