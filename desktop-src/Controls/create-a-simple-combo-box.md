---
title: Создание простого поля со списком
description: В этом разделе описывается создание, Добавление и извлечение элементов из простого поля со списком.
ms.assetid: E432AEC0-6C06-40C7-BBFE-B66C21DB8ACA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4175d435ac78795e7020fd84099d512cc65be20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488349"
---
# <a name="how-to-create-a-simple-combo-box"></a><span data-ttu-id="e931a-103">Создание простого поля со списком</span><span class="sxs-lookup"><span data-stu-id="e931a-103">How to Create a Simple Combo Box</span></span>

<span data-ttu-id="e931a-104">В этом разделе описывается создание, Добавление и извлечение элементов из простого поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-104">This topic describes how to create, add items to, and retrieve items from a simple combo box.</span></span> <span data-ttu-id="e931a-105">В частности, в прилагаемых примерах кода показано, как выполнять следующие функции:</span><span class="sxs-lookup"><span data-stu-id="e931a-105">Specifically, the accompanying code examples demonstrate how to perform the following functions:</span></span>

-   <span data-ttu-id="e931a-106">Динамически создает простое поле со списком в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="e931a-106">Dynamically create a simple combo box in a parent window.</span></span>
-   <span data-ttu-id="e931a-107">Добавьте список элементов в поле со списком и отобразите исходный элемент в поле выбора поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-107">Add a list of items to the combo box and display an initial item in the selection field of the combo box.</span></span>
-   <span data-ttu-id="e931a-108">Определить, когда пользователь выбрал элемент из поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-108">Detect when the user has selected an item from the combo box.</span></span>
-   <span data-ttu-id="e931a-109">Получение выбранного элемента из поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-109">Retrieve the selected item from the combo box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e931a-110">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e931a-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e931a-111">Технологии</span><span class="sxs-lookup"><span data-stu-id="e931a-111">Technologies</span></span>

-   [<span data-ttu-id="e931a-112">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="e931a-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e931a-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e931a-113">Prerequisites</span></span>

-   <span data-ttu-id="e931a-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="e931a-114">C/C++</span></span>
-   <span data-ttu-id="e931a-115">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="e931a-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e931a-116">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e931a-116">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-combo-box"></a><span data-ttu-id="e931a-117">Шаг 1. Создание экземпляра поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-117">Step 1: Create an instance of the combo box.</span></span>

<span data-ttu-id="e931a-118">Пример приложения вызывает функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) для создания дочернего окна окна приложения.</span><span class="sxs-lookup"><span data-stu-id="e931a-118">The example application calls the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a child window of the application window.</span></span> <span data-ttu-id="e931a-119">Стиль [**окна \_ ComboBox WC**](common-control-window-classes.md) указывает, что это поле со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-119">The [**WC\_COMBOBOX**](common-control-window-classes.md) window style specifies that it is a combo box.</span></span>


```C++
// Create the Combobox
//
// Uses the CreateWindow function to create a child window of 
// the application window. The WC_COMBOBOX window style specifies  
// that it is a combobox.

 int xpos = 100;            // Horizontal position of the window.
 int ypos = 100;            // Vertical position of the window.
 int nwidth = 200;          // Width of the window
 int nheight = 200;         // Height of the window
 HWND hwndParent =  m_hwnd; // Handle to the parent window

 HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
     CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
     xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
     NULL);

```



### <a name="step-2-load-the-combo-box-with-the-item-list"></a><span data-ttu-id="e931a-120">Шаг 2. Загрузка поля со списком с списком элементов.</span><span class="sxs-lookup"><span data-stu-id="e931a-120">Step 2: Load the combo box with the item list.</span></span>

<span data-ttu-id="e931a-121">Приложение отправляет сообщение [**\_ ADDSTRING CB**](cb-addstring.md) для каждого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="e931a-121">The application sends a [**CB\_ADDSTRING**](cb-addstring.md) message for each item in the list.</span></span> <span data-ttu-id="e931a-122">После загрузки списка приложение отправляет сообщение [**\_ сеткурсел CB**](cb-setcursel.md) , чтобы отобразить исходный элемент в поле выбора поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-122">After the list is loaded, the application sends the [**CB\_SETCURSEL**](cb-setcursel.md) message to display an initial item in the combo box selection field.</span></span>


```C++
// load the combobox with item list.  
// Send a CB_ADDSTRING message to load each item

TCHAR Planets[9][10] =  
{
    TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
    TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
    TEXT("Pluto??") 
};
       
TCHAR A[16]; 
int  k = 0; 

memset(&A,0,sizeof(A));       
for (k = 0; k <= 8; k += 1)
{
    wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

    // Add string to combobox.
    SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
}
  
// Send the CB_SETCURSEL message to display an initial item 
//  in the selection field  
SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);
```



### <a name="step-3-detect-when-the-user-selects-an-item-and-retrieve-it-from-the-combo-box"></a><span data-ttu-id="e931a-123">Шаг 3. Обнаружение того, когда пользователь выбирает элемент и извлекает его из поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-123">Step 3: Detect when the user selects an item and retrieve it from the combo box.</span></span>

<span data-ttu-id="e931a-124">Когда пользователь делает выбор из списка, поле со списком отправляет уведомление [КБН \_ селчанже](cbn-selchange.md) в родительское окно через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e931a-124">When the user makes a selection from the list, the combo box sends a [CBN\_SELCHANGE](cbn-selchange.md) notification to the parent window via a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="e931a-125">Приложение получает маркер поля со списком из поля *lParam* сообщения уведомления и отправляет сообщение с индексом [**CB \_**](cb-getcursel.md) в поле со списком для получения индекса выбранного элемента списка.</span><span class="sxs-lookup"><span data-stu-id="e931a-125">The application retrieves the handle to the combo box from the *lParam* field of the notification message and sends a [**CB\_GETCURSEL**](cb-getcursel.md) message to the combo box to retrieve the index of the selected list item.</span></span> <span data-ttu-id="e931a-126">После получения индекса элемента приложение отправляет сообщение [**\_ жетлбтекст CB**](cb-getlbtext.md) для получения элемента.</span><span class="sxs-lookup"><span data-stu-id="e931a-126">After obtaining the item index, the application sends a [**CB\_GETLBTEXT**](cb-getlbtext.md) message to get the item.</span></span> <span data-ttu-id="e931a-127">Затем элемент отображается в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="e931a-127">It then displays the item in a message box.</span></span>

> [!Note]  
> <span data-ttu-id="e931a-128">Уведомление [КБН \_ селчанже](cbn-selchange.md) отправляется и обрабатывается до того, как элемент помещается в поле выбора поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e931a-128">The [CBN\_SELCHANGE](cbn-selchange.md) notification is sent and processed before the item is placed in the combo box selection field.</span></span> <span data-ttu-id="e931a-129">Как следствие, в этом примере выбранный элемент не будет отображаться в поле выбора, пока не будет закрыто окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="e931a-129">As result, in this example, the selected item won't appear in selection field until after the message box is closed.</span></span>

 


```C++
switch (message)
{   
    case WM_COMMAND:

        if(HIWORD(wParam) == CBN_SELCHANGE)
        // If the user makes a selection from the list:
        //   Send CB_GETCURSEL message to get the index of the selected list item.
        //   Send CB_GETLBTEXT message to get the item.
        //   Display the item in a messagebox.
        { 
            int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                (WPARAM) 0, (LPARAM) 0);
                TCHAR  ListItem[256];
                (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                (WPARAM) ItemIndex, (LPARAM) ListItem);
            MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
        }
        
        wasHandled = true;
    result = 0;
    break;
```



## <a name="complete-example"></a><span data-ttu-id="e931a-130">Полный пример</span><span class="sxs-lookup"><span data-stu-id="e931a-130">Complete example</span></span>


```C++
// Windows Header Files:
#include <windows.h>
#include <CommCtrl.h>

// C RunTime Header Files
#include <math.h>

#include <objbase.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef Assert
#if defined( DEBUG ) || defined( _DEBUG )
#define Assert(b) if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}
#else
#define Assert(b)
#endif //DEBUG || _DEBUG
#endif


#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT CreateResources();
    void DiscardResources();

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;

 };
```


```C++
#include "SimpleComboBox.h"

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE     /* hInstance */,
    HINSTANCE     /* hPrevInstance */,
    LPSTR     /* lpCmdLine */,
    int     /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                        *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()        
{
    // TODO: Release app resource here.
}

/*******************************************************************
*                                                                  *
*  Create the application window and the combobox.                 *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = TEXT("DemoApp");

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        TEXT("DemoApp"),
        TEXT("Simple Combo Box Example"),
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwnd, SW_SHOWNORMAL);
        UpdateWindow(m_hwnd);
    }


    // Create the Combobox
    //
    // Uses the CreateWindow function to create a child window of 
    // the application window. The WC_COMBOBOX window style specifies  
    // that it is a combobox.

     int xpos = 100;            // Horizontal position of the window.
     int ypos = 100;            // Vertical position of the window.
     int nwidth = 200;          // Width of the window
     int nheight = 200;         // Height of the window
     HWND hwndParent =  m_hwnd; // Handle to the parent window

     HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
         CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
         xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
         NULL);


    
    // load the combobox with item list.  
    // Send a CB_ADDSTRING message to load each item

    TCHAR Planets[9][10] =  
    {
        TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
        TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
        TEXT("Pluto??") 
    };
           
    TCHAR A[16]; 
    int  k = 0; 

    memset(&A,0,sizeof(A));       
    for (k = 0; k <= 8; k += 1)
    {
        wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

        // Add string to combobox.
        SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
    }
      
    // Send the CB_SETCURSEL message to display an initial item 
    //  in the selection field  
    SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);

    return hr;
}


/******************************************************************
*                                                                 *
*  The main window's message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}


/******************************************************************
*                                                                 *
*  The window's message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {   
                case WM_COMMAND:

                    if(HIWORD(wParam) == CBN_SELCHANGE)
                    // If the user makes a selection from the list:
                    //   Send CB_GETCURSEL message to get the index of the selected list item.
                    //   Send CB_GETLBTEXT message to get the item.
                    //   Display the item in a messagebox.
                    { 
                        int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                            (WPARAM) 0, (LPARAM) 0);
                            TCHAR  ListItem[256];
                            (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                            (WPARAM) ItemIndex, (LPARAM) ListItem);
                        MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
                    }
                    
                    wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
```


## <a name="related-topics"></a><span data-ttu-id="e931a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e931a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e931a-132">Сведения о полях со списком</span><span class="sxs-lookup"><span data-stu-id="e931a-132">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="e931a-133">Справочник по элементу управления ComboBox</span><span class="sxs-lookup"><span data-stu-id="e931a-133">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e931a-134">Использование полей со списком</span><span class="sxs-lookup"><span data-stu-id="e931a-134">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="e931a-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="e931a-135">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 