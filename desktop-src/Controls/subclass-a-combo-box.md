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
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="94063-103">Создание подкласса поля со списком</span><span class="sxs-lookup"><span data-stu-id="94063-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="94063-104">В этом разделе показано, как подклассировать поля со списком.</span><span class="sxs-lookup"><span data-stu-id="94063-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="94063-105">Пример приложения C++ создает окно панели инструментов, содержащее два поля со списком.</span><span class="sxs-lookup"><span data-stu-id="94063-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="94063-106">При помощи подклассов элементов управления "поле ввода" в полях со списком окно панели инструментов перехватывает клавиши TAB, ввод и ESC, которые в противном случае будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="94063-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="94063-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="94063-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="94063-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="94063-108">Technologies</span></span>

-   [<span data-ttu-id="94063-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="94063-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="94063-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="94063-110">Prerequisites</span></span>

-   <span data-ttu-id="94063-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="94063-111">C/C++</span></span>
-   <span data-ttu-id="94063-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="94063-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="94063-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="94063-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="94063-114">Обработка сообщения о \_ создании WM</span><span class="sxs-lookup"><span data-stu-id="94063-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="94063-115">Приложение обрабатывает сообщение о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) , чтобы создать два элемента управления "поле со списком" как дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="94063-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


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



<span data-ttu-id="94063-116">Затем приложение подклассировать элементы управления редактирования (поля выбора) в каждом поле со списком, так как они получают символьные данные для простого и раскрывающегося поля со списком.</span><span class="sxs-lookup"><span data-stu-id="94063-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="94063-117">Наконец, он вызывает функцию [**чилдвиндовфромпоинт**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) для получения маркера для каждого элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="94063-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="94063-118">Чтобы создать подкласс для элементов управления "поле ввода", приложение вызывает функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , заменяя указатель на процедуру окна класса указателем на определяемую приложением **субкласспрок** функцию.</span><span class="sxs-lookup"><span data-stu-id="94063-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="94063-119">Указатель на исходную процедуру окна сохраняется в глобальной переменной *лпфнедитвндпрок*.</span><span class="sxs-lookup"><span data-stu-id="94063-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="94063-120">**Субкласспрок** перехватывает клавиши TAB, Enter и ESC и уведомляет окно панели инструментов, отправляя сообщения, определяемые приложением ( \_ вкладка WM, WM \_ ESC и WM \_ Enter).</span><span class="sxs-lookup"><span data-stu-id="94063-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="94063-121">**Субкласспрок** использует функцию [**каллвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) для передачи большинства сообщений в исходную процедуру окна, *лпфнедитвндпрок*.</span><span class="sxs-lookup"><span data-stu-id="94063-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


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



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="94063-122">Обработка сообщения WM \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="94063-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="94063-123">Когда окно панели инструментов получает фокус ввода, оно немедленно устанавливает фокус на первое поле со списком на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="94063-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="94063-124">Для этого в примере вызывается функция [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) в ответ на сообщение [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="94063-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="94063-125">Обработка сообщений Application-Defined</span><span class="sxs-lookup"><span data-stu-id="94063-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="94063-126">Функция **субкласспрок** отправляет определяемые приложением сообщения в окно панели инструментов, когда пользователь нажимает клавишу TAB, ввод или клавишу ESC в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="94063-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="94063-127">Для клавиши TAB отправляется сообщение на **\_ вкладке WM** , сообщение **WM \_ ESC** для клавиши ESC, а для клавиши ВВОД — **сообщение \_ WM** .</span><span class="sxs-lookup"><span data-stu-id="94063-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="94063-128">В примере выполняется обработка сообщения на **\_ вкладке WM** путем установки фокуса на следующее поле со списком на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="94063-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="94063-129">Он обрабатывает сообщение **WM \_ ESC** , передавая фокус главному окну приложения.</span><span class="sxs-lookup"><span data-stu-id="94063-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


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



<span data-ttu-id="94063-130">В ответ на сообщение **о \_ вводе WM** , в примере проверяется допустимость текущего выбора для поля со списком и установка фокуса на главное окно приложения.</span><span class="sxs-lookup"><span data-stu-id="94063-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="94063-131">Если поле со списком не содержит текущего выделения, в примере используется сообщение [**\_ финдстринжексакт CB**](cb-findstringexact.md) для поиска элемента списка, соответствующего содержимому поля выбора.</span><span class="sxs-lookup"><span data-stu-id="94063-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="94063-132">При наличии совпадения в примере задается текущее выделение. в противном случае он добавляет новый элемент списка.</span><span class="sxs-lookup"><span data-stu-id="94063-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


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



## <a name="complete-example"></a><span data-ttu-id="94063-133">Полный пример</span><span class="sxs-lookup"><span data-stu-id="94063-133">Complete example</span></span>

<span data-ttu-id="94063-134">Ниже приведена процедура окна для панели инструментов и процедура подкласса для двух полей со списком.</span><span class="sxs-lookup"><span data-stu-id="94063-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="94063-135">См. также</span><span class="sxs-lookup"><span data-stu-id="94063-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94063-136">Сведения о полях со списком</span><span class="sxs-lookup"><span data-stu-id="94063-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="94063-137">Справочник по элементу управления ComboBox</span><span class="sxs-lookup"><span data-stu-id="94063-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="94063-138">Использование полей со списком</span><span class="sxs-lookup"><span data-stu-id="94063-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="94063-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="94063-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 