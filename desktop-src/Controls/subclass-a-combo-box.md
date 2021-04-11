---
title: Создание подкласса поля со списком
description: В этом разделе показано, как подклассировать поля со списком.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070721"
---
# <a name="how-to-subclass-a-combo-box"></a>Создание подкласса поля со списком

В этом разделе показано, как подклассировать поля со списком. Пример приложения C++ создает окно панели инструментов, содержащее два поля со списком. При помощи подклассов элементов управления "поле ввода" в полях со списком окно панели инструментов перехватывает клавиши TAB, ввод и ESC, которые в противном случае будут игнорироваться.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="process-the-wm_create-message"></a>Обработка сообщения о \_ создании WM

Приложение обрабатывает сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) , чтобы создать два элемента управления "поле со списком" как дочерние окна.


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



Затем приложение подклассировать элементы управления редактирования (поля выбора) в каждом поле со списком, так как они получают символьные данные для простого и раскрывающегося поля со списком. Наконец, он вызывает функцию [**чилдвиндовфромпоинт**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) для получения маркера для каждого элемента управления "поле ввода".

Чтобы создать подкласс для элементов управления "поле ввода", приложение вызывает функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , заменяя указатель на процедуру окна класса указателем на определяемую приложением **субкласспрок** функцию. Указатель на исходную процедуру окна сохраняется в глобальной переменной *лпфнедитвндпрок*.

**Субкласспрок** перехватывает клавиши TAB, Enter и ESC и уведомляет окно панели инструментов, отправляя сообщения, определяемые приложением ( \_ вкладка WM, WM \_ ESC и WM \_ Enter). **Субкласспрок** использует функцию [**каллвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) для передачи большинства сообщений в исходную процедуру окна, *лпфнедитвндпрок*.


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a>Обработка сообщения WM \_ SETFOCUS

Когда окно панели инструментов получает фокус ввода, оно немедленно устанавливает фокус на первое поле со списком на панели инструментов. Для этого в примере вызывается функция [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) в ответ на сообщение [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a>Обработка сообщений Application-Defined

Функция **субкласспрок** отправляет определяемые приложением сообщения в окно панели инструментов, когда пользователь нажимает клавишу TAB, ввод или клавишу ESC в поле со списком. Для клавиши TAB отправляется сообщение на **\_ вкладке WM** , сообщение **WM \_ ESC** для клавиши ESC, а для клавиши ВВОД — **сообщение \_ WM** .

В примере выполняется обработка сообщения на **\_ вкладке WM** путем установки фокуса на следующее поле со списком на панели инструментов. Он обрабатывает сообщение **WM \_ ESC** , передавая фокус главному окну приложения.


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



В ответ на сообщение **о \_ вводе WM** , в примере проверяется допустимость текущего выбора для поля со списком и установка фокуса на главное окно приложения. Если поле со списком не содержит текущего выделения, в примере используется сообщение [**\_ финдстринжексакт CB**](cb-findstringexact.md) для поиска элемента списка, соответствующего содержимому поля выбора. При наличии совпадения в примере задается текущее выделение. в противном случае он добавляет новый элемент списка.


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a>Полный пример

Ниже приведена процедура окна для панели инструментов и процедура подкласса для двух полей со списком.


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения о полях со списком](about-combo-boxes.md)
</dt> <dt>

[Справочник по элементу управления ComboBox](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[Использование полей со списком](using-combo-boxes.md)
</dt> <dt>

[ComboBox](combo-boxes.md)
</dt> </dl>

 

 