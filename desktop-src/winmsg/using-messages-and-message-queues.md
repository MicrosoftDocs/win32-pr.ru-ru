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
# <a name="using-messages-and-message-queues"></a>Использование сообщений и очередей сообщений

В следующих примерах кода показано, как выполнять следующие задачи, связанные с сообщениями Windows и очередями сообщений.

-   [Создание цикла обработки сообщений](#creating-a-message-loop)
-   [Проверка очереди сообщений](#examining-a-message-queue)
-   [Публикация сообщения](#posting-a-message)
-   [Отправка сообщения](#sending-a-message)

## <a name="creating-a-message-loop"></a>Создание цикла обработки сообщений

Система не создает очередь сообщений для каждого потока автоматически. Вместо этого система создает очередь сообщений только для потоков, выполняющих операции, для которых требуется очередь сообщений. Если поток создает одно или несколько окон, необходимо предоставить цикл обработки сообщений. Этот цикл сообщений извлекает сообщения из очереди сообщений потока и отправляет их в соответствующие процедуры окна.

Поскольку система направляет сообщения в отдельные окна приложения, поток должен создать по крайней мере одно окно перед началом цикла обработки сообщений. Большинство приложений содержат один поток, который создает Windows. Типичное приложение регистрирует класс окна для своего главного окна, создает и отображает главное окно, а затем запускает цикл обработки сообщений — все в функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .

Цикл обработки сообщений создается с помощью функций [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) и [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) . Если приложение должно получать символьные данные от пользователя, включите функцию [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) в цикл. **TranslateMessage** преобразует сообщения виртуального ключа в символьные сообщения. В следующем примере показан цикл обработки сообщений в функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) простого приложения на основе Windows.


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



В следующем примере показан цикл обработки сообщений для потока, который использует ускорители и отображает немодальное диалоговое окно. Когда [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) или [**Исдиалогмессаже**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) возвращает **значение true** (указывающее, что сообщение было обработано), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) и [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) не вызываются. Причина в том, что **TranslateAccelerator** и **исдиалогмессаже** выполняют все необходимые преобразования и диспетчеризации сообщений.


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



## <a name="examining-a-message-queue"></a>Проверка очереди сообщений

Иногда приложению необходимо проверить содержимое очереди сообщений потока за пределами цикла обработки сообщений потока. Например, если процедура окна приложения выполняет длительную операцию рисования, может потребоваться, чтобы пользователь мог прерывать операцию. Если приложение периодически не проверяет очередь сообщений во время операции для сообщений мыши и клавиатуры, оно не реагирует на ввод пользователя до тех пор, пока не будет выполнена операция. Причина заключается в том, что функция [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) в цикле обработки сообщений потока не возвращает значение до тех пор, пока процедура окна не завершит обработку сообщения.

Для проверки очереди сообщений во время длительной операции можно использовать функцию [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . **PeekMessage** аналогичен функции "функция- [**сообщение**](/windows/win32/api/winuser/nf-winuser-getmessage) "; Оба варианта проверяют очередь сообщений на наличие сообщения, удовлетворяющего условиям фильтра, а затем копируют сообщение в структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) . Основное различие между этими двумя функциями заключается **в том, что функция** noreturn не возвращает значение, пока в очередь не помещается сообщение, соответствующее условиям фильтра, тогда как **PeekMessage** возвращает немедленно, независимо от того, находится ли сообщение в очереди.

В следующем примере показано, как использовать [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) для проверки очереди сообщений для щелчков мыши и ввода с клавиатуры во время длительной операции.


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



Другие функции, включая [**жеткуеуестатус**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) и [**жетинпутстате**](/windows/win32/api/winuser/nf-winuser-getinputstate), также позволяют проверять содержимое очереди сообщений потока. **Жеткуеуестатус** возвращает массив флагов, указывающих типы сообщений в очереди; его использование — самый быстрый способ определить, содержит ли очередь сообщения. **Жетинпутстате** возвращает **значение true** , если очередь содержит сообщения мыши или клавиатуры. Обе эти функции можно использовать для определения того, содержит ли очередь сообщения, которые необходимо обработать.

## <a name="posting-a-message"></a>Публикация сообщения

Сообщение можно опубликовать в очереди сообщений с помощью функции вывода [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) . **Сообщение** помещает сообщение в конец очереди сообщений потока и сразу же возвращается, не дожидаясь обработки сообщения потоком. Параметры функции включают в себя маркер окна, идентификатор сообщения и два параметра сообщения. Система копирует эти параметры в структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , заполняет элементы **time** и **PT** структуры и помещает структуру в очередь сообщений.

Система использует маркер окна, переданный функцией вывода [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) , для определения того, какая очередь сообщений потока должна принимать сообщение. Если дескриптор является **HWND, \_** то система отправляет сообщение в очереди сообщений потока всех окон верхнего уровня.

Функцию [**постсреадмессаже**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) можно использовать для публикации сообщения в конкретную очередь сообщений потока. **Постсреадмессаже** похож на [**сообщение**](/windows/win32/api/winuser/nf-winuser-postmessagea), за исключением того, что первый параметр является идентификатором потока, а не обработчиком окна. Идентификатор потока можно получить, вызвав функцию [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .

Используйте функцию [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) для выхода из цикла обработки сообщений. **Посткуитмессаже** отправляет сообщение [**о \_ выходе WM Quit**](wm-quit.md) в текущий выполняемый поток. Цикл обработки сообщений потока завершает работу и возвращает управление системе при обнаружении сообщения **WM \_ Quit** . Приложение обычно вызывает **посткуитмессаже** в ответ на сообщение [**WM \_ destroy**](wm-destroy.md) , как показано в следующем примере.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Отправка сообщения

Функция [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) используется для отправки сообщения непосредственно в процедуру окна. **SendMessage** вызывает процедуру окна и ожидает, пока эта процедура обработает сообщение и возвращало результат.

Сообщение может быть отправлено в любое окно в системе; все, что требуется, — это обработчик окна. Система использует этот обработчик, чтобы определить, какая именно оконная процедура должна получить сообщение.

Перед обработкой сообщения, которое могло быть отправлено из другого потока, процедура окна должна сначала вызвать функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) . Если эта функция возвращает **значение true**, то процедура Window должна вызывать [**реплимессаже**](/windows/win32/api/winuser/nf-winuser-replymessage) перед любой функцией, которая приводит к передаче управления потоком, как показано в следующем примере.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



В диалоговом окне можно отправлять несколько сообщений в элементы управления. Эти управляющие сообщения устанавливают внешний вид, поведение и содержимое элементов управления или извлекают сведения об элементах управления. Например, сообщение [**\_ ADDSTRING CB**](../controls/cb-addstring.md) может добавлять строку в поле со списком, а сообщение [**\_ сетчекк BM**](../controls/bm-setcheck.md) может устанавливать состояние флажка или переключателя.

Используйте функцию [**сенддлгитеммессаже**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) для отправки сообщения в элемент управления, указав идентификатор элемента управления и маркер окна диалогового окна, содержащего этот элемент управления. Следующий пример, взятый из процедуры диалогового окна, копирует строку из элемента управления "поле со списком" в его список. В примере **сенддлгитеммессаже** используется для отправки сообщения [**\_ ADDSTRING CB**](../controls/cb-addstring.md) в поле со списком.


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



 

 
