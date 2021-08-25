---
title: Использование сочетаний клавиш
description: В этом разделе рассматриваются задачи, связанные с сочетаниями клавиш.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- Ввод данных пользователем, сочетания клавиш
- захват вводимых пользователем данных, сочетания клавиш
- сочетания клавиш
- Accelerator
- таблицы сочетаний клавиш
- ресурсы таблицы ускорителя
- Функция сочетания клавиш для преобразования
- Сообщение WM_COMMAND
- Сообщение команды WM_SYS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecbb16c92b986cbe73aababc7edc24518cf59ce5009322e3a006bac827427c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886572"
---
# <a name="using-keyboard-accelerators"></a>Использование сочетаний клавиш

В этом разделе рассматриваются задачи, связанные с сочетаниями клавиш.

-   [Использование ресурса таблицы сочетаний клавиш](#using-an-accelerator-table-resource)
    -   [Создание ресурса таблицы ускорителя](#creating-the-accelerator-table-resource)
    -   [Загрузка ресурса таблицы ускорителя](#loading-the-accelerator-table-resource)
    -   [Вызов функции ускорителя преобразования](#calling-the-translate-accelerator-function)
    -   [Обработка \_ командных сообщений WM](/windows)
    -   [Уничтожение ресурса таблицы ускорителя](#destroying-the-accelerator-table-resource)
    -   [Создание ускорителей для атрибутов шрифта](#creating-accelerators-for-font-attributes)
-   [Использование таблицы сочетаний клавиш, созданной во время выполнения](#using-an-accelerator-table-created-at-run-time)
    -   [Создание Run-Time таблицы сочетаний клавиш](#creating-a-run-time-accelerator-table)
    -   [Ускорители обработки](#processing-accelerators)
    -   [Уничтожение таблицы Run-Time Accelerator](#destroying-a-run-time-accelerator-table)
    -   [Создание пользовательских ускорителей редактирования](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Использование ресурса таблицы сочетаний клавиш

Наиболее распространенным способом добавления поддержки ускорителя в приложение является включение ресурса таблицы ускорителя в исполняемый файл приложения, а затем Загрузка ресурса во время выполнения.

В этом разделе рассматриваются следующие темы.

-   [Создание ресурса таблицы ускорителя](#creating-the-accelerator-table-resource)
-   [Загрузка ресурса таблицы ускорителя](#loading-the-accelerator-table-resource)
-   [Вызов функции ускорителя преобразования](#calling-the-translate-accelerator-function)
-   [Обработка \_ командных сообщений WM](/windows)
-   [Уничтожение ресурса таблицы ускорителя](#destroying-the-accelerator-table-resource)
-   [Создание ускорителей для атрибутов шрифта](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Создание ресурса таблицы ускорителя

Ресурс-таблица ускорителя создается с помощью оператора [ускорителей](./accelerators-resource.md) в файле определения ресурсов приложения. Необходимо назначить имя или идентификатор ресурса для таблицы сочетаний клавиш, желательно в отличие от других ресурсов. Система использует этот идентификатор для загрузки ресурса во время выполнения.

Для каждого определяемого сочетания клавиш требуется отдельная запись в таблице сочетаний клавиш. В каждой записи определяется нажатие клавиши (либо код символа ASCII, либо код виртуального ключа), который создает ускоритель и идентификатор ускорителя. Необходимо также указать, следует ли использовать нажатие клавиши в сочетании с клавишами ALT, SHIFT или CTRL. Дополнительные сведения о виртуальных ключах см. в разделе [Ввод с клавиатуры](/windows/desktop/inputdev/keyboard-input).

Клавиша ASCII указывается либо путем заключения символа ASCII в двойные кавычки, либо с помощью целочисленного значения символа в сочетании с флагом ASCII. В следующих примерах показано, как определить ускорители ASCII.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Нажатие клавиши с помощью виртуального ключа определяется по-разному в зависимости от того, является ли клавиша буквенно-цифровым или ключом, отличным от букв и цифр. Для буквенно-цифрового ключа буква или номер ключа, заключенные в двойные кавычки, комбинируется с флагом **VIRTKEY** . Для ключа, не являющегося буквенно-цифровым, код виртуального ключа для конкретного ключа объединяется с флагом **VIRTKEY** . В следующих примерах показано, как определить сочетания клавиш для работы с виртуальными ключами.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

В следующем примере показан ресурс таблицы ускорителя, определяющий ускорители для файловых операций. Имя ресурса — *филеакцел*.

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Если вы хотите, чтобы пользователь нажмет клавиши ALT, SHIFT или CTRL в некоторой комбинации с нажатием клавиши быстрого вызова, укажите ALT, SHIFT и УПРАВЛЯЮЩие флаги в определении ускорителя. Ниже приводятся некоторые примеры.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

По умолчанию, когда сочетание клавиш соответствует пункту меню, система выделяет элемент меню. Для предотвращения выделения отдельных сочетаний клавиш можно использовать флаг **инверсии** . В следующем примере показано, как использовать флаг **инверсии** :

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Чтобы определить ускорители, соответствующие элементам меню в приложении, включите ускорители в текст пунктов меню. В следующем примере показано, как включить ускорители в текст элемента меню в файле определения ресурса.

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a>Загрузка ресурса таблицы ускорителя

Приложение загружает ресурс-таблицу ускорителя, вызывая функцию [**лоадакцелераторс**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) и указывая для приложения обработчик экземпляра, исполняемый файл которого содержит ресурс, а также имя или идентификатор ресурса. **Лоадакцелераторс** загружает указанную таблицу сочетаний клавиш в память и возвращает маркер в таблицу сочетаний клавиш.

Приложение может загрузить ресурс таблицы ускорителя в любое время. Как правило, приложение с одним потоком загружает свою таблицу сочетаний клавиш перед входом в основной цикл обработки сообщений. Приложение, использующее несколько потоков, обычно загружает ресурс-таблицу ускорителя для потока перед входом в цикл обработки сообщений для потока. Приложение или поток может также использовать несколько таблиц сочетаний клавиш, каждый из которых связан с определенным окном в приложении. Такое приложение загрузит таблицу сочетаний клавиш для окна каждый раз, когда пользователь активировал окно. Дополнительные сведения о потоках см. в разделе [процессы и потоки](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Вызов функции ускорителя преобразования

Чтобы обработать ускорители, цикл обработки сообщений приложения (или потока) должен содержать вызов функции [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . **TranslateAccelerator** сравнивает нажатия клавиш с таблицей сочетаний клавиш и, если находит совпадение, преобразует нажатия клавиш в сообщение [**\_ Command WM**](wm-command.md) (или [**WM \_ сискомманд**](wm-syscommand.md)). Затем функция отправляет сообщение в процедуру окна. Параметры функции **TranslateAccelerator** включают в себя маркер окна, который получает сообщения **\_ команды WM** , обработчик для таблицы сочетаний клавиш, используемый для преобразования ускорителей, и указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение из очереди. В следующем примере показано, как вызвать **TranslateAccelerator** из цикла обработки сообщений.


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a>Обработка \_ командных сообщений WM

При использовании сочетания клавиш окно, указанное в функции [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , получает [**\_ команду WM**](wm-command.md) или сообщение [**\_ сискомманд WM**](wm-syscommand.md) . Слово низкого порядка параметра *wParam* содержит идентификатор ускорителя. Процедура окна проверяет идентификатор, чтобы определить источник сообщения **\_ команды WM** и обработать сообщение соответствующим образом.

Как правило, если ускоритель соответствует пункту меню в приложении, элементу сочетания клавиш и пункта меню назначается один и тот же идентификатор. Если необходимо узнать, было ли [**\_ командное сообщение WM**](wm-command.md) создано ускорителем или пунктом меню, можно проверить слово в высоком порядке в параметре *wParam* . Если сообщение создано ускорителем, то его значение в высоком порядке равно 1. Если сообщение создано элементом меню, то его значение в верхнем порядке равно 0.

### <a name="destroying-the-accelerator-table-resource"></a>Уничтожение ресурса таблицы ускорителя

Система автоматически уничтожает ресурсы таблицы ускорителя, загруженные функцией [**лоадакцелераторс**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , удаляя ресурс из памяти после закрытия приложения.

### <a name="creating-accelerators-for-font-attributes"></a>Создание ускорителей для атрибутов шрифта

В примере в этом разделе показано, как выполнять следующие задачи:

-   Создайте ресурс-таблицу ускорителя.
-   Загрузка таблицы сочетаний клавиш во время выполнения.
-   Преобразование ускорителей в цикле обработки сообщений.
-   Обработка [**\_ командных сообщений WM**](wm-command.md) , созданных ускорителями.

Эти задачи демонстрируются в контексте приложения, которое содержит меню **символов** и соответствующие ускорители, позволяющие пользователю выбирать атрибуты текущего шрифта.

В следующей части файла определения ресурсов определяется меню « **символ** » и связанная таблица сочетаний клавиш. Обратите внимание, что пункты меню показывают клавиши быстрого вызова и что каждый ускоритель имеет тот же идентификатор, что и соответствующий пункт меню.


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



В следующих разделах из исходного файла приложения показано, как реализовать ускорители.


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a>Использование таблицы сочетаний клавиш, созданной во время выполнения

В этом разделе описывается использование таблиц сочетаний клавиш, созданных во время выполнения.

-   [Создание Run-Time таблицы сочетаний клавиш](#creating-a-run-time-accelerator-table)
-   [Ускорители обработки](#processing-accelerators)
-   [Уничтожение таблицы Run-Time Accelerator](#destroying-a-run-time-accelerator-table)
-   [Создание пользовательских ускорителей редактирования](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Создание Run-Time таблицы сочетаний клавиш

Первым шагом при создании таблицы сочетаний клавиш во время выполнения является заполнение массива несамостоятельных [**структур.**](/windows/win32/api/winuser/ns-winuser-accel) Каждая структура в массиве определяет ускоритель в таблице. Определение ускорителя включает его флаги, ключ и идентификатор. Структура **для** рассогласования имеет следующий вид.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Вы определяете нажатие клавиши быстрого вызова, указывая код символа ASCII или код виртуальной клавиши в **ключевом** [**элементе структуры доступа**](/windows/win32/api/winuser/ns-winuser-accel) . Если указан код виртуального ключа, необходимо сначала включить флаг **фвирткэй** в член **фвирт** . в противном случае система интерпретирует код как код символа ASCII. Можно включить флаг **фконтрол**, **ФАЛТ** или **фшифт** или все три, чтобы объединить клавиши CTRL, Alt или SHIFT с нажатием клавиши.

Чтобы создать таблицу сочетаний клавиш, передайте указатель на массив несамостоятельных [**структур в**](/windows/win32/api/winuser/ns-winuser-accel) функцию [**креатеакцелератортабле**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . **Креатеакцелератортабле** создает таблицу сочетаний клавиш и возвращает маркер в таблицу.

### <a name="processing-accelerators"></a>Ускорители обработки

Процесс загрузки и вызова ускорителей, предоставляемых таблицей ускорителя, созданной во время выполнения, аналогичен процессу обработки, предоставляемой ресурсом таблицы ускорителя. Дополнительные сведения см. [в разделе Загрузка ресурса таблицы ускорителя](#loading-the-accelerator-table-resource) с помощью [обработки \_ командных сообщений WM](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Уничтожение таблицы Run-Time Accelerator

Система автоматически уничтожает таблицы ускорителя, созданные во время выполнения, удаляя ресурсы из памяти после закрытия приложения. Можно уничтожить таблицу сочетаний клавиш и удалить ее из памяти раньше, передав маркер таблицы в функцию [**дестройакцелератортабле**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

### <a name="creating-user-editable-accelerators"></a>Создание пользовательских ускорителей редактирования

В этом примере показано, как создать диалоговое окно, позволяющее пользователю изменить сочетание клавиш, связанное с пунктом меню. Диалоговое окно состоит из поля со списком, содержащего пункты меню, поле со списком, содержащее имена ключей, и флажки для выбора клавиш CTRL, ALT и SHIFT. На следующем рисунке показано диалоговое окно.

![диалоговое окно с полями со списком и флажками](images/useredit.gif)

В следующем примере показано, как диалоговое окно определено в файле определения ресурса.

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

Строка меню приложения содержит подменю **символов** с элементами, с которыми связаны сочетания клавиш.

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

Значения пунктов меню для шаблона меню являются константами, определенными в файле заголовка приложения.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

В диалоговом окне используется массив определяемых приложением структур ключ, каждый из которых содержит текстовую строку с клавиатуры и текстовую строку сочетания клавиш. При создании диалогового окна он анализирует массив и добавляет каждую строку текста нажатия клавиши в поле со списком **Выбор нажатия клавиши** . Когда пользователь нажимает кнопку **ОК** , диалоговое окно ищет выбранную текстовую строку нажатия клавиши и получает соответствующую текстовую строку ускорителя. В диалоговом окне добавляется текстовая строка ускорителя к тексту выбранного пользователем пункта меню. В следующем примере показан массив структурных ключ:


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



Процедура инициализации диалогового окна заполняет **элемент Выбор** и выбирает поля со списком **нажатия клавиш** . После того как пользователь выберет пункт меню и связанный ускоритель, диалоговое окно проверит элементы управления в диалоговом окне, чтобы получить выбор пользователя, обновляет текст пункта меню, а затем создает новую таблицу сочетаний клавиш, содержащую определяемый пользователем новый ускоритель. В следующем примере показана процедура диалогового окна. Обратите внимание, что в процедуре окна необходимо инициализировать.


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 