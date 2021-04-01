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
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="5acd4-104">Создание элемента управления "горячий ключ"</span><span class="sxs-lookup"><span data-stu-id="5acd4-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="5acd4-105">В этом разделе показано, как создать элемент управления горячей клавиши.</span><span class="sxs-lookup"><span data-stu-id="5acd4-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="5acd4-106">Элемент управления "горячий ключ" создается с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , которая указывает \_ класс окна класса горячих клавиш.</span><span class="sxs-lookup"><span data-stu-id="5acd4-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5acd4-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="5acd4-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5acd4-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="5acd4-108">Technologies</span></span>

-   [<span data-ttu-id="5acd4-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="5acd4-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5acd4-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5acd4-110">Prerequisites</span></span>

-   <span data-ttu-id="5acd4-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="5acd4-111">C/C++</span></span>
-   <span data-ttu-id="5acd4-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="5acd4-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5acd4-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="5acd4-113">Instructions</span></span>


<span data-ttu-id="5acd4-114">Перед созданием элемента управления горячими ключами убедитесь, что библиотека DLL общих элементов управления загружена.</span><span class="sxs-lookup"><span data-stu-id="5acd4-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="5acd4-115">В следующем примере кода C++ функция, определяемая приложением, вызывает функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) для загрузки библиотеки DLL общего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5acd4-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="5acd4-116">Затем вызывается функция [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указывающая **клавишу \_** класс окна класса, для создания элемента управления горячим ключом.</span><span class="sxs-lookup"><span data-stu-id="5acd4-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="5acd4-117">Он использует сообщения [**ХКМ \_ Сетрулес**](hkm-setrules.md) и [**ХКМ \_ сесоткэй**](hkm-sethotkey.md) для инициализации элемента управления и возвращает в него маркер.</span><span class="sxs-lookup"><span data-stu-id="5acd4-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="5acd4-118">Этот элемент управления горячими ключами не позволяет пользователю выбрать горячую клавишу, которая является одним немодифицированным ключом, и не разрешает пользователю выбирать только SHIFT и ключ.</span><span class="sxs-lookup"><span data-stu-id="5acd4-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="5acd4-119">Эти правила эффективно запрещают пользователю выбирать горячие клавиши, которые могут быть случайно указаны при вводе текста.</span><span class="sxs-lookup"><span data-stu-id="5acd4-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="5acd4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="5acd4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5acd4-121">Ссылка на элемент управления ключами</span><span class="sxs-lookup"><span data-stu-id="5acd4-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5acd4-122">Сведения об элементах управления горячей клавиши</span><span class="sxs-lookup"><span data-stu-id="5acd4-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="5acd4-123">Использование элементов управления горячими ключами</span><span class="sxs-lookup"><span data-stu-id="5acd4-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 