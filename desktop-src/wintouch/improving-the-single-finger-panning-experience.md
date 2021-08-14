---
title: Улучшение возможностей панорамирования Single-Finger
description: при создании приложения, предназначенного для Windows Touch, оно автоматически обеспечивает базовую поддержку панорамирования. Однако можно использовать \_ сообщение жеста WM, чтобы обеспечить улучшенную поддержку панорамирования с одним пальцем.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Сенсорное панорамирование с одним пальцем
- Windows Сенсорный ввод, панорамирование
- Windows Сенсорный ввод, полосы прокрутки
- Windows Касание, жесты
- Windows Сенсорные сообщения жестов
- Windows Сенсорный ввод, обратная связь
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
ms.openlocfilehash: cf740d673e8bd2d2711238902d3de6c89d21a01fe330524b910db050011872f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435447"
---
# <a name="improving-the-single-finger-panning-experience"></a>Улучшение возможностей панорамирования Single-Finger

при создании приложения, предназначенного для Windows Touch, оно автоматически обеспечивает базовую поддержку панорамирования. Однако можно использовать сообщение [**\_ жеста WM**](wm-gesture.md) , чтобы обеспечить улучшенную поддержку панорамирования с одним пальцем.

## <a name="overview"></a>Обзор

Чтобы улучшить возможности панорамирования с одним пальцем, выполните следующие действия, как описано в последующих разделах этой статьи:

-   Создание приложения с полосами прокрутки и отключенными жестами.
-   Добавлена поддержка сообщений Pan для жестов.
-   Включить Bounce.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Создание приложения с полосами прокрутки и отключенными жестами

Прежде чем начать, необходимо создать приложение с полосами прокрутки. Этот процесс объясняется в разделе [поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md) . Если вы хотите начать с примера содержимого, перейдите к этому разделу и создайте приложение с полосами прокрутки, а затем отключите жесты. Если у вас уже есть приложение с работающими полосами прокрутки, отключите жесты, как описано в этом разделе.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Добавление пользовательской поддержки панорамирования для сообщений с жестами Pan

Для поддержки сообщений Pan жеста их необходимо реализовать в методе **WndProc** . Сообщения жестов используются для определения горизонтальных и вертикальных различий для сообщений PAN. Разность используется для обновления объекта полосы прокрутки, который обновляет пользовательский интерфейс.

сначала обновите параметры версии Windows в файле targetver. h, чтобы включить Windows Touch. в следующем коде показаны различные параметры версии Windows, которые должны заменить их в targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Затем добавьте в проект файл Укссеме. h и добавьте библиотеку укссеме. lib в дополнительные зависимости проекта.


```C++
#include <uxtheme.h>
```



Затем добавьте следующие переменные в начало функции **WndProc** . Они будут использоваться в вычислениях для панорамирования.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Затем добавьте обработчик для сообщения [**\_ жеста WM**](wm-gesture.md) , чтобы полосы прокрутки обновлялись с разностью на основе жестов панорамирования. Это обеспечивает более детализированный контроль панорамирования.

Следующий код получает структуру [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) из *lParam*, сохраняет последнюю координату y из структуры и определяет изменение позиций для обновления объекта полосы прокрутки. Следующий код должен быть помещен в оператор switch для **WndProc** .


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



Теперь, когда вы выполняете жест панорамирования в окне, вы увидите, что текст прокручивается с помощью инерции. На этом этапе может потребоваться изменить текст так, чтобы в нем было больше строк, чтобы можно было изучить раскрутку больших фрагментов текста.

## <a name="boundary-feedback-in-wndproc"></a>Отзыв о границе в WndProc

Обратная связь — это тип визуальной обратной связи, предоставляемой пользователям, когда они достигают конца области паннабле. Он активируется приложением при достижении границы. В предыдущем примере с помощью сообщения [**\_ жеста WM**](wm-gesture.md) условие End `(si.nPos == si.yPos)` из варианта **\_ жеста WM** используется для проверки достижения конца паннабле региона. Следующие переменные используются для трассировки значений и ошибок тестирования.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



Вариант жеста сдвига обновляется для активации обратной связи. Следующий код иллюстрирует вариант **\_ сдвига GID** из обработчика [**сообщений \_ жестов WM**](wm-gesture.md) .


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



Теперь окно приложения должно иметь обратную связь, когда пользователь прокручивается за нижнюю часть области полосы прокрутки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Сенсорные жесты](guide-multi-touch-gestures.md)
</dt> <dt>

[**бегинпаннингфидбакк**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**ендпаннингфидбакк**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**упдатепаннингфидбакк**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 