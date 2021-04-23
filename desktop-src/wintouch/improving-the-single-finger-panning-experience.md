---
title: Улучшение возможностей панорамирования Single-Finger
description: При создании приложения, предназначенного для Windows Touch, оно автоматически обеспечивает базовую поддержку панорамирования. Однако можно использовать \_ сообщение жеста WM, чтобы обеспечить улучшенную поддержку панорамирования с одним пальцем.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Сенсорные экраны Windows, панорамирование одним пальцем
- Касание Windows, панорамирование
- Касание Windows, полосы прокрутки
- Касание Windows, жесты
- Касание Windows, сообщения с жестами Pan
- Касание Windows, обратная связь
- Панорамирование одним пальцем
- панорамирование, одиночный палец
- панорамирование, обратная связь
- полосы прокрутки, панорамирование одним пальцем
- жесты, панорамирование одним пальцем
- полосы прокрутки, отключение
- жесты, отключение
- жесты, сообщения Pan жестов
- панорамирование, сообщения для сдвига жестов
- Отзывы о границах, панорамирование одним пальцем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792163"
---
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="b1220-120">Улучшение возможностей панорамирования Single-Finger</span><span class="sxs-lookup"><span data-stu-id="b1220-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="b1220-121">При создании приложения, предназначенного для Windows Touch, оно автоматически обеспечивает базовую поддержку панорамирования.</span><span class="sxs-lookup"><span data-stu-id="b1220-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="b1220-122">Однако можно использовать сообщение [**\_ жеста WM**](wm-gesture.md) , чтобы обеспечить улучшенную поддержку панорамирования с одним пальцем.</span><span class="sxs-lookup"><span data-stu-id="b1220-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="b1220-123">Обзор</span><span class="sxs-lookup"><span data-stu-id="b1220-123">Overview</span></span>

<span data-ttu-id="b1220-124">Чтобы улучшить возможности панорамирования с одним пальцем, выполните следующие действия, как описано в последующих разделах этой статьи:</span><span class="sxs-lookup"><span data-stu-id="b1220-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="b1220-125">Создание приложения с полосами прокрутки и отключенными жестами.</span><span class="sxs-lookup"><span data-stu-id="b1220-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="b1220-126">Добавлена поддержка сообщений Pan для жестов.</span><span class="sxs-lookup"><span data-stu-id="b1220-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="b1220-127">Включить Bounce.</span><span class="sxs-lookup"><span data-stu-id="b1220-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="b1220-128">Создание приложения с полосами прокрутки и отключенными жестами</span><span class="sxs-lookup"><span data-stu-id="b1220-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="b1220-129">Прежде чем начать, необходимо создать приложение с полосами прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b1220-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="b1220-130">Этот процесс объясняется в разделе [поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="b1220-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="b1220-131">Если вы хотите начать с примера содержимого, перейдите к этому разделу и создайте приложение с полосами прокрутки, а затем отключите жесты.</span><span class="sxs-lookup"><span data-stu-id="b1220-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="b1220-132">Если у вас уже есть приложение с работающими полосами прокрутки, отключите жесты, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b1220-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="b1220-133">Добавление пользовательской поддержки панорамирования для сообщений с жестами Pan</span><span class="sxs-lookup"><span data-stu-id="b1220-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="b1220-134">Для поддержки сообщений Pan жеста их необходимо реализовать в методе **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="b1220-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="b1220-135">Сообщения жестов используются для определения горизонтальных и вертикальных различий для сообщений PAN.</span><span class="sxs-lookup"><span data-stu-id="b1220-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="b1220-136">Разность используется для обновления объекта полосы прокрутки, который обновляет пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b1220-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="b1220-137">Сначала обновите параметры версии Windows в файле targetver. h, чтобы включить Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="b1220-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="b1220-138">В следующем коде показаны различные параметры версии Windows, которые должны заменить их в targetver. h.</span><span class="sxs-lookup"><span data-stu-id="b1220-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="b1220-139">Затем добавьте в проект файл Укссеме. h и добавьте библиотеку укссеме. lib в дополнительные зависимости проекта.</span><span class="sxs-lookup"><span data-stu-id="b1220-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="b1220-140">Затем добавьте следующие переменные в начало функции **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="b1220-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="b1220-141">Они будут использоваться в вычислениях для панорамирования.</span><span class="sxs-lookup"><span data-stu-id="b1220-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="b1220-142">Затем добавьте обработчик для сообщения [**\_ жеста WM**](wm-gesture.md) , чтобы полосы прокрутки обновлялись с разностью на основе жестов панорамирования.</span><span class="sxs-lookup"><span data-stu-id="b1220-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="b1220-143">Это обеспечивает более детализированный контроль панорамирования.</span><span class="sxs-lookup"><span data-stu-id="b1220-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="b1220-144">Следующий код получает структуру [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) из *lParam*, сохраняет последнюю координату y из структуры и определяет изменение позиций для обновления объекта полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b1220-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="b1220-145">Следующий код должен быть помещен в оператор switch для **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="b1220-145">The following code should be placed in your **WndProc** switch statement.</span></span>


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



<span data-ttu-id="b1220-146">Теперь, когда вы выполняете жест панорамирования в окне, вы увидите, что текст прокручивается с помощью инерции.</span><span class="sxs-lookup"><span data-stu-id="b1220-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="b1220-147">На этом этапе может потребоваться изменить текст так, чтобы в нем было больше строк, чтобы можно было изучить раскрутку больших фрагментов текста.</span><span class="sxs-lookup"><span data-stu-id="b1220-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="b1220-148">Отзыв о границе в WndProc</span><span class="sxs-lookup"><span data-stu-id="b1220-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="b1220-149">Обратная связь — это тип визуальной обратной связи, предоставляемой пользователям, когда они достигают конца области паннабле.</span><span class="sxs-lookup"><span data-stu-id="b1220-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="b1220-150">Он активируется приложением при достижении границы.</span><span class="sxs-lookup"><span data-stu-id="b1220-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="b1220-151">В предыдущем примере с помощью сообщения [**\_ жеста WM**](wm-gesture.md) условие End `(si.nPos == si.yPos)` из варианта **\_ жеста WM** используется для проверки достижения конца паннабле региона.</span><span class="sxs-lookup"><span data-stu-id="b1220-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="b1220-152">Следующие переменные используются для трассировки значений и ошибок тестирования.</span><span class="sxs-lookup"><span data-stu-id="b1220-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="b1220-153">Вариант жеста сдвига обновляется для активации обратной связи.</span><span class="sxs-lookup"><span data-stu-id="b1220-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="b1220-154">Следующий код иллюстрирует вариант **\_ сдвига GID** из обработчика [**сообщений \_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="b1220-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



<span data-ttu-id="b1220-155">Теперь окно приложения должно иметь обратную связь, когда пользователь прокручивается за нижнюю часть области полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b1220-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1220-156">См. также</span><span class="sxs-lookup"><span data-stu-id="b1220-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1220-157">Сенсорные жесты Windows</span><span class="sxs-lookup"><span data-stu-id="b1220-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="b1220-158">**бегинпаннингфидбакк**</span><span class="sxs-lookup"><span data-stu-id="b1220-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="b1220-159">**ендпаннингфидбакк**</span><span class="sxs-lookup"><span data-stu-id="b1220-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="b1220-160">**упдатепаннингфидбакк**</span><span class="sxs-lookup"><span data-stu-id="b1220-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 