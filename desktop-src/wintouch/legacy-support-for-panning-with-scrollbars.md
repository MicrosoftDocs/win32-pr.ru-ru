---
title: Устаревшая поддержка панорамирования с помощью полос прокрутки
description: В этом разделе описывается поддержка панорамирования с помощью полос прокрутки в приложениях на основе Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch, поддержка прежних версий
- панорамирование с помощью полос прокрутки
- Касание Windows, панорамирование с помощью полос прокрутки
- Касание Windows, полосы прокрутки
- полосы прокрутки, панорамирование
- полосы прокрутки, поддержка прежних версий
- Касание Windows, жесты
- жесты, панорамирование с помощью полос прокрутки
- Касание Windows, жесты
- жесты, панорамирование с помощью полос прокрутки
- жесты, отключение
- Касание Windows, сообщения колесика мыши
- сообщения колесика мыши
- Касание Windows, Настройка панорамирования
- панорамирование, полосы прокрутки
- панорамирование, поддержка прежних версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104554370"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a><span data-ttu-id="38dae-119">Устаревшая поддержка панорамирования с помощью полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="38dae-119">Legacy Support for Panning with Scroll Bars</span></span>

<span data-ttu-id="38dae-120">В этом разделе описывается поддержка панорамирования с помощью полос прокрутки в приложениях на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="38dae-120">This section describes support for panning using scroll bars in Windows-based applications.</span></span>

<span data-ttu-id="38dae-121">В Windows 7 жесты панорамирования формируют \_ \* сообщения прокрутки WM, чтобы включить устаревшую поддержку панорамирования.</span><span class="sxs-lookup"><span data-stu-id="38dae-121">In Windows 7, panning gestures generate WM\_\*SCROLL messages to enable legacy support for panning.</span></span> <span data-ttu-id="38dae-122">Так как приложения могут не поддерживать все \_ \* сообщения прокрутки WM, панорамирование может работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="38dae-122">Because your applications may not support all of the WM\_\*SCROLL messages, panning may not work correctly.</span></span> <span data-ttu-id="38dae-123">В этом разделе описаны действия, которые необходимо выполнить, чтобы обеспечить функционирование устаревших возможностей панорамирования в приложениях по мере ожидания пользователей.</span><span class="sxs-lookup"><span data-stu-id="38dae-123">This topic describes the steps you must take to ensure that the legacy panning experience in applications functions as users expect.</span></span>

## <a name="overview"></a><span data-ttu-id="38dae-124">Обзор</span><span class="sxs-lookup"><span data-stu-id="38dae-124">Overview</span></span>

<span data-ttu-id="38dae-125">В следующих разделах объясняется, как включить прежний режим панорамирования:</span><span class="sxs-lookup"><span data-stu-id="38dae-125">The following sections explain how to enable the legacy panning experience:</span></span>

-   <span data-ttu-id="38dae-126">Создание приложения с полосами прокрутки.</span><span class="sxs-lookup"><span data-stu-id="38dae-126">Create an application with scroll bars.</span></span>
-   <span data-ttu-id="38dae-127">Отключить жесты.</span><span class="sxs-lookup"><span data-stu-id="38dae-127">Disable flicks.</span></span>
-   <span data-ttu-id="38dae-128">Настройка возможностей панорамирования.</span><span class="sxs-lookup"><span data-stu-id="38dae-128">Customize the panning experience.</span></span>

## <a name="create-an-application-with-scroll-bars"></a><span data-ttu-id="38dae-129">Создание приложения с полосами прокрутки</span><span class="sxs-lookup"><span data-stu-id="38dae-129">Create an Application with Scroll Bars</span></span>

<span data-ttu-id="38dae-130">Запустите новый проект Win32 с помощью мастера Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38dae-130">Start a new Win32 project using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="38dae-131">Убедитесь, что для типа приложения задано приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="38dae-131">Make sure the application type is set to the Windows application.</span></span> <span data-ttu-id="38dae-132">Вам не нужно включать поддержку библиотеки активных шаблонов (ATL).</span><span class="sxs-lookup"><span data-stu-id="38dae-132">You don't need to enable support for the Active Template Library (ATL).</span></span> <span data-ttu-id="38dae-133">На следующем рисунке показано, как будет выглядеть проект после его запуска.</span><span class="sxs-lookup"><span data-stu-id="38dae-133">The following image shows what your project will look like after you have started it.</span></span>

![снимок экрана с окном без полос прокрутки](images/gpd-1.png)

<span data-ttu-id="38dae-135">Затем включите полосы прокрутки изображения.</span><span class="sxs-lookup"><span data-stu-id="38dae-135">Next, enable scroll bars on the image.</span></span> <span data-ttu-id="38dae-136">Измените код создания окна в **InitInstance** , чтобы вызов функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) создал окно с полосами прокрутки.</span><span class="sxs-lookup"><span data-stu-id="38dae-136">Change the window creation code in **InitInstance** so that the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function call creates a window with scroll bars.</span></span> <span data-ttu-id="38dae-137">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="38dae-137">The following code shows how to do this.</span></span>


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



<span data-ttu-id="38dae-138">После изменения кода создания окна приложение будет иметь полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="38dae-138">After you have changed the window creation code, your application will have a scroll bar.</span></span> <span data-ttu-id="38dae-139">На следующем рисунке показано, как приложение может взглянуть на этот момент.</span><span class="sxs-lookup"><span data-stu-id="38dae-139">The following image shows how the application might look at this point.</span></span>

![снимок экрана, показывающий окно с вертикальной полосой прокрутки, но без текста](images/gpd-2.png)

<span data-ttu-id="38dae-141">После изменения кода создания окна Добавьте в приложение объект полосы прокрутки и прокрутите его часть текста.</span><span class="sxs-lookup"><span data-stu-id="38dae-141">After you have changed the window creation code, add a scroll bar object to your application and some text to scroll.</span></span> <span data-ttu-id="38dae-142">Поместите следующий код в начало метода **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="38dae-142">Place the following code into the top of the **WndProc** method.</span></span>


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



<span data-ttu-id="38dae-143">Затем реализуйте логику приложения для настройки вычислений текста для метрик текста.</span><span class="sxs-lookup"><span data-stu-id="38dae-143">Next, implement the application logic for configuring the text calculations for text metrics.</span></span> <span data-ttu-id="38dae-144">Следующий код должен заменить существующий случай **\_ создания WM** в функции **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="38dae-144">The following code should replace the existing **WM\_CREATE** case in the **WndProc** function.</span></span>


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



<span data-ttu-id="38dae-145">Затем реализуйте логику приложения для повторного вычисления текстового блока при изменении размера окна.</span><span class="sxs-lookup"><span data-stu-id="38dae-145">Next, implement the application logic for recalculation of the text block when the window is resized.</span></span> <span data-ttu-id="38dae-146">Следующий код следует поместить в параметр Message в **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="38dae-146">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



<span data-ttu-id="38dae-147">Затем реализуйте логику приложения для вертикальных сообщений прокрутки.</span><span class="sxs-lookup"><span data-stu-id="38dae-147">Next, implement the application logic for vertical scroll messages.</span></span> <span data-ttu-id="38dae-148">Следующий код следует поместить в параметр Message в **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="38dae-148">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



<span data-ttu-id="38dae-149">Затем обновите код, чтобы перерисовать окно.</span><span class="sxs-lookup"><span data-stu-id="38dae-149">Next, update the code to redraw the window.</span></span> <span data-ttu-id="38dae-150">Следующий код должен заменить стандартный регистр **WM \_ Paint** в **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="38dae-150">The following code should replace the default **WM\_PAINT** case in **WndProc**.</span></span>


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



<span data-ttu-id="38dae-151">Теперь при сборке и запуске приложения у него должен быть стандартный текст и вертикальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="38dae-151">Now when you build and run your application, it should have the boilerplate text and a vertical scroll bar.</span></span> <span data-ttu-id="38dae-152">На следующем рисунке показано, как может выглядеть приложение.</span><span class="sxs-lookup"><span data-stu-id="38dae-152">The following image shows how your application might look.</span></span>

![снимок экрана, показывающий окно с вертикальной полосой прокрутки и текстом](images/gpd-3.png)

## <a name="disable-flicks"></a><span data-ttu-id="38dae-154">Отключить жесты</span><span class="sxs-lookup"><span data-stu-id="38dae-154">Disable Flicks</span></span>

<span data-ttu-id="38dae-155">Чтобы улучшить возможности панорамирования в приложении, необходимо отключить жесты.</span><span class="sxs-lookup"><span data-stu-id="38dae-155">To improve the panning experience in your application, you should turn off flicks.</span></span> <span data-ttu-id="38dae-156">Для этого задайте свойства окна для значения *HWND* при его инициализации.</span><span class="sxs-lookup"><span data-stu-id="38dae-156">To do this, set window properties on the *hWnd* value when it is initialized.</span></span> <span data-ttu-id="38dae-157">Значения, используемые для жестов, хранятся в заголовке тпкшрд. h, который также необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="38dae-157">The values used for flicks are stored in the tpcshrd.h header, which also must be included.</span></span> <span data-ttu-id="38dae-158">Следующий код следует поместить в директивы include и в функцию **InitInstance** после создания *HWND*.</span><span class="sxs-lookup"><span data-stu-id="38dae-158">The following code should be placed in your include directives and in the **InitInstance** function after you have created your *hWnd*.</span></span>

> [!Note]  
> <span data-ttu-id="38dae-159">Это полезно для приложений, для которых требуется немедленная обратная связь с событием касания или пером, а не для проверки порогового значения времени или расстояния.</span><span class="sxs-lookup"><span data-stu-id="38dae-159">This is useful for applications that require immediate feedback on a touch or pen down event instead of testing for a time or distance threshold.</span></span>

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a><span data-ttu-id="38dae-160">Настройка возможностей панорамирования</span><span class="sxs-lookup"><span data-stu-id="38dae-160">Customize the Panning Experience</span></span>

<span data-ttu-id="38dae-161">По умолчанию может потребоваться разный режим панорамирования по сравнению с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38dae-161">You might want a different panning experience than Windows 7 offers by default.</span></span> <span data-ttu-id="38dae-162">Чтобы повысить удобство панорамирования, необходимо добавить обработчик для сообщения [**\_ жеста WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="38dae-162">To improve the panning experience, you must add the handler for the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="38dae-163">Дополнительные сведения см. [в разделе улучшение возможностей панорамирования Single-Finger](improving-the-single-finger-panning-experience.md).</span><span class="sxs-lookup"><span data-stu-id="38dae-163">For more information, see [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="38dae-164">См. также</span><span class="sxs-lookup"><span data-stu-id="38dae-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38dae-165">Сенсорные жесты Windows</span><span class="sxs-lookup"><span data-stu-id="38dae-165">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 