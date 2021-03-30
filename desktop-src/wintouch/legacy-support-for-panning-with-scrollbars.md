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
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Устаревшая поддержка панорамирования с помощью полос прокрутки

В этом разделе описывается поддержка панорамирования с помощью полос прокрутки в приложениях на основе Windows.

В Windows 7 жесты панорамирования формируют \_ \* сообщения прокрутки WM, чтобы включить устаревшую поддержку панорамирования. Так как приложения могут не поддерживать все \_ \* сообщения прокрутки WM, панорамирование может работать неправильно. В этом разделе описаны действия, которые необходимо выполнить, чтобы обеспечить функционирование устаревших возможностей панорамирования в приложениях по мере ожидания пользователей.

## <a name="overview"></a>Обзор

В следующих разделах объясняется, как включить прежний режим панорамирования:

-   Создание приложения с полосами прокрутки.
-   Отключить жесты.
-   Настройка возможностей панорамирования.

## <a name="create-an-application-with-scroll-bars"></a>Создание приложения с полосами прокрутки

Запустите новый проект Win32 с помощью мастера Microsoft Visual Studio. Убедитесь, что для типа приложения задано приложение Windows. Вам не нужно включать поддержку библиотеки активных шаблонов (ATL). На следующем рисунке показано, как будет выглядеть проект после его запуска.

![снимок экрана с окном без полос прокрутки](images/gpd-1.png)

Затем включите полосы прокрутки изображения. Измените код создания окна в **InitInstance** , чтобы вызов функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) создал окно с полосами прокрутки. В следующем примере кода показано, как это сделать:


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



После изменения кода создания окна приложение будет иметь полосу прокрутки. На следующем рисунке показано, как приложение может взглянуть на этот момент.

![снимок экрана, показывающий окно с вертикальной полосой прокрутки, но без текста](images/gpd-2.png)

После изменения кода создания окна Добавьте в приложение объект полосы прокрутки и прокрутите его часть текста. Поместите следующий код в начало метода **WndProc** .


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



Затем реализуйте логику приложения для настройки вычислений текста для метрик текста. Следующий код должен заменить существующий случай **\_ создания WM** в функции **WndProc** .


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



Затем реализуйте логику приложения для повторного вычисления текстового блока при изменении размера окна. Следующий код следует поместить в параметр Message в **WndProc**.


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



Затем реализуйте логику приложения для вертикальных сообщений прокрутки. Следующий код следует поместить в параметр Message в **WndProc**.


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



Затем обновите код, чтобы перерисовать окно. Следующий код должен заменить стандартный регистр **WM \_ Paint** в **WndProc**.


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



Теперь при сборке и запуске приложения у него должен быть стандартный текст и вертикальная полоса прокрутки. На следующем рисунке показано, как может выглядеть приложение.

![снимок экрана, показывающий окно с вертикальной полосой прокрутки и текстом](images/gpd-3.png)

## <a name="disable-flicks"></a>Отключить жесты

Чтобы улучшить возможности панорамирования в приложении, необходимо отключить жесты. Для этого задайте свойства окна для значения *HWND* при его инициализации. Значения, используемые для жестов, хранятся в заголовке тпкшрд. h, который также необходимо добавить. Следующий код следует поместить в директивы include и в функцию **InitInstance** после создания *HWND*.

> [!Note]  
> Это полезно для приложений, для которых требуется немедленная обратная связь с событием касания или пером, а не для проверки порогового значения времени или расстояния.

 


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



## <a name="customize-the-panning-experience"></a>Настройка возможностей панорамирования

По умолчанию может потребоваться разный режим панорамирования по сравнению с Windows 7. Чтобы повысить удобство панорамирования, необходимо добавить обработчик для сообщения [**\_ жеста WM**](wm-gesture.md) . Дополнительные сведения см. [в разделе улучшение возможностей панорамирования Single-Finger](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сенсорные жесты Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 