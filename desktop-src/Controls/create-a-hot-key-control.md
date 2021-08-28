---
title: Создание элемента управления "горячий ключ"
description: В этом разделе показано, как создать элемент управления горячей клавиши. Элемент управления "горячий ключ" создается с помощью функции CreateWindowEx, которая указывает \_ класс окна класса горячих клавиш.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081db39f07e8d80fcbb5a437bc8cbe83473b4299282c8b2437d95acda02b2db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577046"
---
# <a name="how-to-create-a-hot-key-control"></a>Создание элемента управления "горячий ключ"

В этом разделе показано, как создать элемент управления горячей клавиши. Элемент управления "горячий ключ" создается с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , которая указывает \_ класс окна класса горячих клавиш.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на элемент управления ключами](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Сведения об элементах управления горячей клавиши](hot-key-controls.md)
</dt> <dt>

[Использование элементов управления горячими ключами](using-hot-key-controls.md)
</dt> </dl>

 

 