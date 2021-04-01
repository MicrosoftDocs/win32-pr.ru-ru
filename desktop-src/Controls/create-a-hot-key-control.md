---
title: Создание элемента управления "горячий ключ"
description: В этом разделе показано, как создать элемент управления горячей клавиши. Элемент управления "горячий ключ" создается с помощью функции CreateWindowEx, которая указывает \_ класс окна класса горячих клавиш.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891264"
---
# <a name="how-to-create-a-hot-key-control"></a>Создание элемента управления "горячий ключ"

В этом разделе показано, как создать элемент управления горячей клавиши. Элемент управления "горячий ключ" создается с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , которая указывает \_ класс окна класса горячих клавиш.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Перед созданием элемента управления горячими ключами убедитесь, что библиотека DLL общих элементов управления загружена.

В следующем примере кода C++ функция, определяемая приложением, вызывает функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) для загрузки библиотеки DLL общего элемента управления. Затем вызывается функция [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указывающая **клавишу \_** класс окна класса, для создания элемента управления горячим ключом. Он использует сообщения [**ХКМ \_ Сетрулес**](hkm-setrules.md) и [**ХКМ \_ сесоткэй**](hkm-sethotkey.md) для инициализации элемента управления и возвращает в него маркер.

Этот элемент управления горячими ключами не позволяет пользователю выбрать горячую клавишу, которая является одним немодифицированным ключом, и не разрешает пользователю выбирать только SHIFT и ключ. Эти правила эффективно запрещают пользователю выбирать горячие клавиши, которые могут быть случайно указаны при вводе текста.



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на элемент управления ключами](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Сведения об элементах управления горячей клавиши](hot-key-controls.md)
</dt> <dt>

[Использование элементов управления горячими ключами](using-hot-key-controls.md)
</dt> </dl>

 

 