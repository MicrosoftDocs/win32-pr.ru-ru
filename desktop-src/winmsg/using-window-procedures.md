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
# <a name="using-window-procedures"></a>Использование оконных процедур

В этом разделе описывается выполнение следующих задач, связанных с процедурами окон.

-   [Разработка процедуры окна](#designing-a-window-procedure)
-   [Связывание оконной процедуры с классом окна](#associating-a-window-procedure-with-a-window-class)
-   [Подклассировать окно](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Разработка процедуры окна

В следующем примере показана структура типичной процедуры окна. В процедуре окна используется аргумент Message в операторе **switch** с отдельными сообщениями, обрабатываемыми отдельными инструкциями **case** . Обратите внимание, что каждый вариант возвращает определенное значение для каждого сообщения. Для сообщений, которые не обрабатываются, процедура Window вызывает функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .


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



Сообщение [**WM \_ нккреате**](wm-nccreate.md) отправляется сразу после создания окна, но если приложение отвечает на это сообщение, возвращая **значение false**, функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) завершается ошибкой. Сообщение [**о \_ создании WM**](wm-create.md) отправляется после того, как окно уже создано.

Сообщение [**WM \_ destroy**](wm-destroy.md) отправляется, когда окно собирается уничтожиться. Функция [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) выполняет удаление всех дочерних окон удаляемого окна. Сообщение [**WM \_ нкдестрой**](wm-ncdestroy.md) отправляется непосредственно перед уничтожением окна.

Как минимум, процедура окна должна обрабатывать сообщение [**WM \_ Paint**](../gdi/wm-paint.md) для рисования самого себя. Обычно он также обрабатывает сообщения мыши и клавиатуры. Ознакомьтесь с описанием отдельных сообщений, чтобы определить, должна ли эта процедура работать с ними.

Приложение может вызвать функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в процессе обработки сообщения. В этом случае приложение может изменить параметры сообщения перед передачей сообщения в **дефвиндовпрок** или продолжить обработку по умолчанию после выполнения собственных операций.

Процедура диалогового окна получает сообщение [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) вместо сообщения [**WM \_ CREATE**](wm-create.md) и не передает необработанные сообщения в функцию [**дефдлгпрок**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) . В противном случае процедура диалогового окна совпадает с процедурой окна.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Связывание оконной процедуры с классом окна

Вы связываете процедуру окна с классом окна при регистрации класса. Необходимо заполнить структуру [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) данными о классе, а член **лпфнвндпрок** должен указывать адрес процедуры окна. Чтобы зарегистрировать класс, передайте в функцию [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) адрес структуры **вндкласс** . После регистрации класса окна процедура окна автоматически связывается с каждым новым окном, созданным с помощью этого класса.

В следующем примере показано, как связать процедуру окна в предыдущем примере с классом окна.


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



## <a name="subclassing-a-window"></a>Подклассировать окно

Чтобы создать подкласс экземпляра окна, вызовите функцию [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) и укажите в окне маркер, чтобы создать подкласс \_ флага ГВЛ WndProc и указатель на процедуру-подкласс. **SetWindowLong** возвращает указатель на исходную процедуру окна; Используйте этот указатель для передачи сообщений в исходную процедуру. Процедура окна подкласса должна использовать функцию [**каллвиндовпрок**](/windows/win32/api/winuser/nf-winuser-callwindowproca) для вызова исходной процедуры окна.

> [!Note]  
> Чтобы написать код, совместимый как с 32-разрядными, так и с 64-разрядными версиями Windows, используйте функцию [**сетвиндовлонгптр**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .

 

В следующем примере показано, как создать подкласс экземпляра элемента управления "поле ввода" в диалоговом окне. Процедура окна подкласса позволяет элементу управления "поле ввода" получать все вводы с клавиатуры, включая клавиши ENTER и TAB, когда элемент управления имеет фокус ввода.


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



 

 
