---
title: начало работы с помощью сенсорных жестов Windows
description: В этом разделе описаны основные шаги для использования жестов Мультисенсорная.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Касание Windows, жесты
- Касание Windows, сообщения
- жесты, сведения
- жесты, сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410653"
---
# <a name="getting-started-with-windows-touch-gestures"></a><span data-ttu-id="d3cbb-107">начало работы с помощью сенсорных жестов Windows</span><span class="sxs-lookup"><span data-stu-id="d3cbb-107">Getting Started with Windows Touch Gestures</span></span>

<span data-ttu-id="d3cbb-108">В этом разделе описаны основные шаги для использования жестов Мультисенсорная.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-108">This section describes the basic steps for using multitouch gestures.</span></span>

<span data-ttu-id="d3cbb-109">При использовании жестов касания Windows обычно выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-109">The following steps are typically performed when using Windows Touch gestures:</span></span>

1.  <span data-ttu-id="d3cbb-110">Настройка окна для получения жестов.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-110">Set up a window for receiving gestures.</span></span>
2.  <span data-ttu-id="d3cbb-111">Обрабатывает сообщения жестов.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-111">Handle the gesture messages.</span></span>
3.  <span data-ttu-id="d3cbb-112">Интерпретировать сообщения жестов.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-112">Interpret the gesture messages.</span></span>

## <a name="setting-up-a-window-to-receive-gestures"></a><span data-ttu-id="d3cbb-113">Настройка окна для получения жестов</span><span class="sxs-lookup"><span data-stu-id="d3cbb-113">Setting up a Window to Receive Gestures</span></span>

<span data-ttu-id="d3cbb-114">По умолчанию вы получаете [**сообщения \_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="d3cbb-114">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="d3cbb-115">При вызове [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)вы перестанете получать [**сообщения \_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="d3cbb-115">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="d3cbb-116">Если вы не получаете сообщения **\_ жестов WM** , убедитесь, что вы не вызывали **регистертаучвиндов**.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-116">If you are not receiving **WM\_GESTURE** messages, make sure that you haven't called **RegisterTouchWindow**.</span></span>

 

<span data-ttu-id="d3cbb-117">В следующем коде показана простая реализация InitInstance.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-117">The following code shows a simple InitInstance implementation.</span></span>


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a><span data-ttu-id="d3cbb-118">Обработка сообщений жестов</span><span class="sxs-lookup"><span data-stu-id="d3cbb-118">Handling Gesture Messages</span></span>

<span data-ttu-id="d3cbb-119">Аналогично обработке сообщений сенсорного ввода Windows можно обрабатывать сообщения жестов различными способами.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-119">Similar to handling Windows Touch input messages, you can handle gesture messages in many ways.</span></span> <span data-ttu-id="d3cbb-120">Если вы используете Win32, вы можете проверить сообщение [**\_ жеста WM**](wm-gesture.md) в WndProc.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-120">If you are using Win32, you can check for the [**WM\_GESTURE**](wm-gesture.md) message in WndProc.</span></span> <span data-ttu-id="d3cbb-121">При создании приложения другого типа можно добавить в схему сообщений сообщение **\_ жеста WM** , а затем реализовать пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-121">If you are creating another type of application, you can add the **WM\_GESTURE** message to the message map and then implement a custom handler.</span></span>

<span data-ttu-id="d3cbb-122">В следующем коде показано, как можно обработать сообщения жестов.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-122">The following code shows how gesture messages could be handled.</span></span>


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a><span data-ttu-id="d3cbb-123">Интерпретация сообщений жестов</span><span class="sxs-lookup"><span data-stu-id="d3cbb-123">Interpreting the Gesture Messages</span></span>

<span data-ttu-id="d3cbb-124">Функция [**жетжестуреинфо**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) используется для интерпретации сообщения жеста в структуру, описывающую жест.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-124">The [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) function is used to interpret a gesture message into a structure describing the gesture.</span></span> <span data-ttu-id="d3cbb-125">Структура [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)содержит сведения о жесте, например расположение, в котором был выполнен жест, и тип жеста.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-125">The structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), has information about the gesture such as the location where the gesture was performed and the type of gesture.</span></span> <span data-ttu-id="d3cbb-126">В следующем коде показано, как можно получить и интерпретировать сообщение жеста.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-126">The following code shows how you can retrieve and interpret a gesture message.</span></span>


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a><span data-ttu-id="d3cbb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d3cbb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3cbb-128">Сенсорные жесты Windows</span><span class="sxs-lookup"><span data-stu-id="d3cbb-128">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




