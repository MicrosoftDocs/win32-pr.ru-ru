---
title: Создание многострочного элемента управления Edit
description: В этом разделе показано, как реализовать простой текстовый редактор путем добавления многострочного элемента управления Edit в клиентскую область окна.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988001"
---
# <a name="how-to-create-a-multiline-edit-control"></a><span data-ttu-id="e0d14-103">Создание многострочного элемента управления Edit</span><span class="sxs-lookup"><span data-stu-id="e0d14-103">How to Create a Multiline Edit Control</span></span>

<span data-ttu-id="e0d14-104">В этом разделе показано, как реализовать простой текстовый редактор путем добавления многострочного элемента управления Edit в клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="e0d14-104">This topic demonstrates how to implement a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="e0d14-105">С помощью многострочного элемента управления "поле ввода" пользователь может выбрать команду изменить команды в меню.</span><span class="sxs-lookup"><span data-stu-id="e0d14-105">By using the multiline edit control, the user can select edit commands from a menu.</span></span> <span data-ttu-id="e0d14-106">Эти команды позволяют пользователю выполнять простые операции редактирования, такие как Отмена предыдущего действия, Вырезание или копирование выделенных фрагментов в буфер обмена, вставка текста из буфера обмена и удаление текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="e0d14-106">These commands enable the user to perform simple editing operations such as undo a previous action, cut or copy selections to the clipboard, paste text from the clipboard, and delete the current selection.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e0d14-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e0d14-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e0d14-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="e0d14-108">Technologies</span></span>

-   [<span data-ttu-id="e0d14-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="e0d14-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e0d14-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e0d14-110">Prerequisites</span></span>

-   <span data-ttu-id="e0d14-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="e0d14-111">C/C++</span></span>
-   <span data-ttu-id="e0d14-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="e0d14-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e0d14-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e0d14-113">Instructions</span></span>


<span data-ttu-id="e0d14-114">Приложение должно включать код для создания экземпляра и инициализации многострочного элемента управления Edit, а затем обрабатывать команды редактирования пользователя.</span><span class="sxs-lookup"><span data-stu-id="e0d14-114">Your application must include code to create an instance of and initialize a multiline edit control and then process user edit commands.</span></span>

<span data-ttu-id="e0d14-115">В следующем примере кода C++ реализована большая часть функциональных возможностей простого текстового процессора путем добавления многострочного элемента управления Edit в клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="e0d14-115">The following C++ code example implements much of the functionality of a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="e0d14-116">Система автоматически выполняет операции переноса слов для элемента управления "поле ввода", а также обрабатывает обработку для вертикальной полосы прокрутки (созданной путем указания [**ES \_ аутовскролл**](edit-control-styles.md) в вызове функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).</span><span class="sxs-lookup"><span data-stu-id="e0d14-116">The system automatically performs wordwrap operations for the edit control and also handles the processing for the vertical scroll bar (created by specifying [**ES\_AUTOVSCROLL**](edit-control-styles.md) in the call to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function).</span></span>

<span data-ttu-id="e0d14-117">Команды редактирования пользователя отправляются в оконный процесс через сообщения [**\_ командной строки WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e0d14-117">User edit commands are sent to the window process via [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages.</span></span>

> [!Note]  
> <span data-ttu-id="e0d14-118">Если окно содержит ленту Windows, размер элемента управления "поле ввода" должен быть скорректирован в соответствии с высотой ленты.</span><span class="sxs-lookup"><span data-stu-id="e0d14-118">If the window includes the Windows Ribbon, the size of the edit control must be adjusted to accommodate the height of the Ribbon.</span></span> <span data-ttu-id="e0d14-119">Дополнительные сведения см. в разделе [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span><span class="sxs-lookup"><span data-stu-id="e0d14-119">For more information, see [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span></span>

 



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



## <a name="related-topics"></a><span data-ttu-id="e0d14-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e0d14-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0d14-121">Сведения об элементах управления "Изменить"</span><span class="sxs-lookup"><span data-stu-id="e0d14-121">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="e0d14-122">Изменить ссылку на элемент управления</span><span class="sxs-lookup"><span data-stu-id="e0d14-122">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e0d14-123">Использование элементов управления Edit</span><span class="sxs-lookup"><span data-stu-id="e0d14-123">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="e0d14-124">Изменить элемент управления</span><span class="sxs-lookup"><span data-stu-id="e0d14-124">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 