---
title: Создание многострочного элемента управления Edit
description: В этом разделе показано, как реализовать простой текстовый редактор путем добавления многострочного элемента управления Edit в клиентскую область окна.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11100d4d6f82c7a352d4ddacaa7fc05694b4d54125febc766a6d3f1c68376e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829075"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Создание многострочного элемента управления Edit

В этом разделе показано, как реализовать простой текстовый редактор путем добавления многострочного элемента управления Edit в клиентскую область окна. С помощью многострочного элемента управления "поле ввода" пользователь может выбрать команду изменить команды в меню. Эти команды позволяют пользователю выполнять простые операции редактирования, такие как Отмена предыдущего действия, Вырезание или копирование выделенных фрагментов в буфер обмена, вставка текста из буфера обмена и удаление текущего выделения.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Приложение должно включать код для создания экземпляра и инициализации многострочного элемента управления Edit, а затем обрабатывать команды редактирования пользователя.

В следующем примере кода C++ реализована большая часть функциональных возможностей простого текстового процессора путем добавления многострочного элемента управления Edit в клиентскую область окна. Система автоматически выполняет операции переноса слов для элемента управления "поле ввода", а также обрабатывает обработку для вертикальной полосы прокрутки (созданной путем указания [**ES \_ аутовскролл**](edit-control-styles.md) в вызове функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).

Команды редактирования пользователя отправляются в оконный процесс через сообщения [**\_ командной строки WM**](/windows/desktop/menurc/wm-command) .

> [!Note]  
> если окно содержит ленту Windows, размер элемента управления "поле ввода" должен быть скорректирован в соответствии с высотой ленты. дополнительные сведения см. в статье [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об элементах управления "Изменить"](about-edit-controls.md)
</dt> <dt>

[Изменить ссылку на элемент управления](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Использование элементов управления Edit](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Изменить элемент управления](edit-controls.md)
</dt> </dl>

 

 