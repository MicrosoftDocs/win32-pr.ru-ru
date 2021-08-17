---
description: В примерах этого раздела описывается выполнение задач, связанных с использованием Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Использование Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75681987a4bc012618135f666b3ff973880b8129d2ad1ee896bcdbed266d179d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436970"
---
# <a name="using-windows"></a>Использование Windows

В примерах этого раздела описывается выполнение следующих задач.

-   [Создание главного окна](#creating-a-main-window)
-   [Создание, перечисление и изменение размеров дочерних Windows](#creating-enumerating-and-sizing-child-windows)
-   [Уничтожение окна](#destroying-a-window)
-   [Использование многоуровневых Windows](#using-layered-windows)

## <a name="creating-a-main-window"></a>Создание главного окна

Первое окно, создаваемое приложением, обычно является главным окном. Главное окно создается с помощью функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) с указанием класса окна, имени окна, стилей окна, размера, расположения, маркера меню, маркера экземпляра и данных для создания. Главное окно относится к классу окон, определяемому приложением, поэтому необходимо зарегистрировать класс окна и предоставить оконную процедуру для класса перед созданием главного окна.

Большинство приложений обычно используют стиль [**WS \_ оверлаппедвиндов**](window-styles.md) для создания главного окна. Этот стиль дает окну строку заголовка, меню окна, границу изменения размера, а также кнопки сворачивания и развертывания. Функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) возвращает маркер, который однозначно идентифицирует окно.

В следующем примере создается главное окно, принадлежащее классу окна, определяемому приложением. Имя окна, **главное окно**, появится в заголовке окна. Комбинируя стили [**WS \_ VSCROLL**](window-styles.md) и **WS \_ HSCROLL** с стилем **WS \_ оверлаппедвиндов** , приложение создает главное окно с горизонтальной и вертикальной полосами прокрутки в дополнение к компонентам, предоставляемым стилем **WS \_ оверлаппедвиндов** . Четыре вхождения константы **\_ Уседефаулт во Вт** . устанавливают исходный размер и расположение окна в значения по умолчанию, определяемые системой. При указании **значения NULL** вместо маркера меню окно будет иметь меню, определенное для класса Window.


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



Обратите внимание, что в предыдущем примере функция [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) вызывается после создания главного окна. Это делается потому, что система не отображает автоматически главное окно после его создания. Передавая флаг **SW \_ Шовдефаулт** в **ShowWindow**, приложение позволяет программе, запустившего приложение, установить начальное состояние отображения главного окна. Функция [**упдатевиндов**](/windows/win32/api/winuser/nf-winuser-updatewindow) отправляет окну свое первое сообщение [**WM \_ Paint**](../gdi/wm-paint.md) .

## <a name="creating-enumerating-and-sizing-child-windows"></a>Создание, перечисление и изменение размеров дочерних Windows

Вы можете разделить клиентскую область окна на разные функциональные области с помощью дочерних окон. Создание дочернего окна похоже на создание главного окна — используется функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Чтобы создать окно класса, определяемого приложением, необходимо зарегистрировать класс окна и предоставить процедуру окна перед созданием дочернего окна. Необходимо предоставить дочернему окну стиль дочернего окна [**WS \_**](window-styles.md) и указать родительское окно для дочернего окна при его создании.

В следующем примере клиентская область главного окна приложения делится на три функциональные области путем создания трех дочерних окон одинакового размера. Каждое дочернее окно имеет ту же высоту, что и клиентскую область главного окна, но каждая из них имеет одну треть ее ширину. Главное окно создает дочерние окна в ответ на сообщение [**о \_ создании WM**](wm-create.md) , которое основное окно получает в процессе создания окна. Так как у каждого дочернего окна есть стиль [**\_ границы WS**](window-styles.md) , у каждого из них есть тонкая граница. Кроме того, поскольку стиль " **WS \_ Visible** " не указан, каждое дочернее окно изначально скрыто. Кроме того, обратите внимание, что каждому дочернему окну назначается идентификатор дочернего окна.

Основное окно изменяет размеры и положение дочерних окон в ответ на сообщение о [**\_ размере WM**](wm-size.md) , которое основное окно получает при изменении его размера. В ответ на **\_ изменение размера WM** главное окно получает размеры клиентской области с помощью функции [**жетклиентрект**](/windows/win32/api/winuser/nf-winuser-getclientrect) , а затем передает измерения в функцию [**енумчилдвиндовс**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) . **Енумчилдвиндовс** передает этот обработчик в каждое дочернее окно, в свою очередь, в функцию обратного вызова [**енумчилдпрок**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) , определяемую приложением. Эта функция изменяет размеры и положение каждого дочернего окна, вызывая функцию [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) . Размер и расположение основаны на измерениях клиентской области главного окна и идентификаторе дочернего окна. После этого **енумчилдпрок** вызывает функцию [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) , чтобы сделать окно видимым.


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



## <a name="destroying-a-window"></a>Уничтожение окна

Для уничтожения окна можно использовать функцию [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) . Как правило, приложение отправляет сообщение [**о \_ закрытии WM**](wm-close.md) перед уничтожением окна, предоставляя ему возможность запросить подтверждение перед уничтожением окна. Окно, содержащее меню "окно", автоматически получает сообщение о **\_ закрытии WM** при нажатии пользователем кнопки " **Закрыть** " в меню "окно". Если пользователь подтверждает, что окно должно быть уничтожено, приложение вызывает **дестройвиндов**. Система отправляет сообщение [**WM \_ destroy**](wm-destroy.md) в окно после его удаления с экрана. В ответ на попытку **WM \_ destroy** окно сохраняет свои данные и освобождает все выделенные ресурсы. Главное окно завершает обработку **WM \_ destroy** , вызывая функцию [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) для выхода из приложения.

В следующем примере показано, как запросить подтверждение пользователя перед уничтожением окна. В ответ на [**запрос WM \_ Close**](wm-close.md)в примере отображается диалоговое окно, содержащее кнопки **Да**, **нет** и **Отмена** . Если пользователь нажмет кнопку **Да**, вызывается [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) . в противном случае окно не уничтожается. Так как окно, которое уничтожается, является главным окном, пример вызывает [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) в ответ на функцию [**WM \_ destroy**](wm-destroy.md).


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



## <a name="using-layered-windows"></a>Использование многоуровневых Windows

Чтобы диалоговое окно поступало в виде полупрозрачного окна, сначала создайте диалоговое окно, как обычно. Затем в [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md)задайте многоуровневый бит расширенного стиля окна и вызовите [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) с нужным альфа-значением. Код может выглядеть следующим образом:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Обратите внимание, что третий параметр [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) имеет значение в диапазоне от 0 до 255, и 0 делает окно полностью прозрачным и 255 делает его полностью непрозрачным. Этот параметр имитирует более гибкую [**блендфунктион**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) функции [**алфабленд**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .

Чтобы сделать это окно полностью непрозрачным, удалите **\_ \_ Многоуровневый бит WS ex** , вызвав [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , а затем запросите окно для перерисовки. Удаление бита необходимо, чтобы система могла понять, что она может освободить некоторый объем памяти, связанный с разслойом и перенаправлением. Код может выглядеть следующим образом:


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



чтобы использовать многоуровневые дочерние окна, приложение должно объявить себя Windows 8 в манифесте.

 

 
