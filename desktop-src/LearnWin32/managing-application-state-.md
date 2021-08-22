---
title: Управление состоянием приложения
description: Оконная процедура — это просто функция, которая вызывается для каждого сообщения, поэтому она по сути не имеет состояния. Поэтому необходим способ отслеживания состояния приложения от одного вызова функции к следующему.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0cde27195ba0dfc16668da11beac243821902995a9d01daa337f8962944343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068072"
---
# <a name="managing-application-state"></a>Управление состоянием приложения

Оконная процедура — это просто функция, которая вызывается для каждого сообщения, поэтому она по сути не имеет состояния. Поэтому необходим способ отслеживания состояния приложения от одного вызова функции к следующему.

Самый простой подход — просто поместить все в глобальные переменные. Это хорошо подходит для небольших программ, и многие из примеров пакета SDK используют этот подход. Однако в большой программе она приводит к распространению глобальных переменных. Кроме того, у вас может быть несколько окон, каждая из которых имеет собственную процедуру окна. Отслеживание того, какое окно должно иметь доступ, какие переменные становятся запутанными и подвержены ошибкам.

Функция [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) предоставляет способ передачи любой структуры данных в окно. При вызове этой функции в оконную процедуру отправляются следующие два сообщения:

- [**WM \_ нккреате**](/windows/desktop/winmsg/wm-nccreate)
- [**\_Создание WM**](/windows/desktop/winmsg/wm-create)

Эти сообщения отправляются в указанном порядке. (Они не являются единственными двумя сообщениями, отправленными во время [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), но мы можем игнорировать другие для этого обсуждения.)

Сообщение [**WM \_ Нккреате**](/windows/desktop/winmsg/wm-nccreate) и [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) отправляются до того, как окно станет видимым. Это делает их хорошим местом для инициализации пользовательского интерфейса, например, для определения первоначального макета окна.

Последний параметр [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) является указателем типа **void \** _. В этом параметре можно передать любое значение указателя. Когда процедура окна обрабатывает сообщение [_ *WM \_ нккреате* *](/windows/desktop/winmsg/wm-nccreate) или [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) , оно может извлекать это значение из данных сообщения.

Давайте посмотрим, как использовать этот параметр для передачи данных приложения в окно. Сначала определите класс или структуру, которые содержат сведения о состоянии.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

При вызове [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)передайте указатель на эту структуру в последнем параметре **void \*** .

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

Когда вы получаете сообщения [**\_ Нккреате**](/windows/desktop/winmsg/wm-nccreate) и [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) , параметр *lParam* каждого сообщения является указателем на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . Структура **CREATESTRUCT** , в свою очередь, содержит указатель, переданный в [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

![Схема, на которой показан макет структуры CREATESTRUCT](images/appstate01.png)

Вот как можно извлечь указатель на структуру данных. Сначала получите структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) путем приведения параметра *lParam* .

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

Элемент **лпкреатепарамс** структуры [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) является исходным указателем void, указанным в [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Получите указатель на собственную структуру данных путем приведения **лпкреатепарамс**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Затем вызовите функцию [**сетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) и передайте указатель в структуру данных.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

Цель последнего вызова функции — сохранить указатель *статеинфо* в данных экземпляра для окна. После этого вы всегда можете вернуть указатель из окна, вызвав [**жетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Каждое окно имеет свои данные экземпляра, поэтому можно создать несколько окон и присвоить каждому окну собственный экземпляр структуры данных. Этот подход особенно удобен, если вы определяете класс Windows и создаете более одного окна этого класса, например, при создании пользовательского класса элемента управления. В небольшой вспомогательной функции удобно обернуть вызов [**жетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) .

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

Теперь можно написать процедуру окна следующим образом.

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

## <a name="an-object-oriented-approach"></a>Object-Orientedный подход

Этот подход можно расширить. Мы уже определили структуру данных для хранения сведений о состоянии окна. Имеет смысл предоставить эту структуру данных с помощью функций-членов (методов), которые работают с данными. Это естественно ведет к проектированию, где структура (или класс) отвечает за все операции в окне. Затем процедура окна станет частью класса.

Другими словами, мы хотели бы проделать следующее:

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

На эту:

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

Единственная проблема заключается в том, как подключить `MyWindow::WindowProc` метод. Функция [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) ждет, что процедура окна является указателем на функцию. Нельзя передать указатель на функцию-член (не статическую) в этом контексте. Однако можно передать указатель на *статическую* функцию-член, а затем делегировать ее функции-члену. Ниже приведен шаблон класса, демонстрирующий этот подход:

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

`BaseWindow`Класс является абстрактным базовым классом, от которого наследуются определенные классы окон. Например, ниже приведено объявление простого класса, производного от `BaseWindow` :

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Чтобы создать окно, вызовите `BaseWindow::Create` :

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

`BaseWindow::HandleMessage`Для реализации процедуры окна используется чистый виртуальный метод. Например, следующая реализация эквивалентна процедуре окна, показанной в начале [модуля 1](your-first-windows-program.md).

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

Обратите внимание, что дескриптор окна хранится в переменной-члене (*m \_ HWND*), поэтому нам не нужно передавать его в качестве параметра в `HandleMessage` .

многие из существующих Windows платформ программирования, таких как Microsoft Foundation Classes (MFC) и библиотека atl, используют подходы, похожие на показанные здесь. Конечно, полностью обобщенная платформа, такая как MFC, сложнее, чем этот сравнительно простой пример.

## <a name="next"></a>Следующая

[модуль 2. использование COM в программе Windows](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Связанные темы

[Пример Басевиндов](basewindow-sample.md)