---
title: Прокрутка текста
description: В этом разделе описываются изменения, которые можно внести в главное окно приложения, чтобы разрешить пользователю прокручивать текст.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2139ac1bff3d197d63011e6a6e76c861b984c5e20b5c54ceab8871678d31a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914224"
---
# <a name="how-to-scroll-text"></a>Прокрутка текста

В этом разделе описываются изменения, которые можно внести в главное окно приложения, чтобы разрешить пользователю прокручивать текст. В примере в этом разделе создается и отображается массив текстовых строк, а также обрабатываются сообщения [**\_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) полосы прокрутки, чтобы пользователь мог прокручивать текст как по вертикали, так и по горизонтали.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="processing-the-wm_create-message"></a>Обработка сообщения о \_ создании WM

Единицы прокрутки обычно задаются при обработке сообщения о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) . Удобно основывать единицы прокрутки по измерениям шрифта, связанного с контекстом устройства (DC) окна. Чтобы получить размеры шрифта для определенного контроллера домена, используйте функцию [**жеттекстметрикс**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) .

В примере в этом разделе одна вертикальная единица прокрутки эквивалентна высоте ячейки символов, а также внешним ведущим. Одна горизонтальная единица прокрутки эквивалентна средней ширине ячейки символов. Поэтому позиции горизонтальной прокрутки не соответствуют фактическим символам, если экранный шрифт не имеет фиксированной ширины.

### <a name="processing-the-wm_size-message"></a>Обработка сообщения о \_ размере WM

При обработке сообщения [**о \_ размере WM**](/windows/desktop/winmsg/wm-size) удобно настроить диапазон прокрутки и расположение прокрутки, чтобы отразить размеры клиентской области, а также количество строк текста, которые будут отображены.

Функция [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) задает минимальные и максимальные значения позиций, размер страницы и расположение прокрутки для полосы прокрутки.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Обработка сообщений WM \_ HSCROLL и WM \_ VSCROLL

Полоса прокрутки отправляет сообщения [**WM \_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) в оконную процедуру всякий раз, когда пользователь щелкает полосу прокрутки или перетаскивает ползунок. Неупорядоченные слова **WM \_ VSCROLL** и **WM \_ HSCROLL** содержат код запроса, который указывает направление и величину действия прокрутки.

При обработке сообщений [**WM \_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) проверяется код запроса полосы прокрутки, а шаг прокрутки вычисляется. После применения приращения к текущей положении прокрутки окно прокручивается до новой позицией с помощью функции [**скроллвиндовекс**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) , а расположение ползунка корректируется с помощью функции [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .

После прокрутки окна часть его клиентской области становится недействительной. Чтобы обеспечить обновление недопустимого региона, функция [**упдатевиндов**](/windows/desktop/api/winuser/nf-winuser-updatewindow) используется для создания сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .

### <a name="processing-the-wm_paint-message"></a>Обработка сообщения WM \_ Paint

При обработке сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) удобно нарисовать строки текста, которые должны отображаться в недействительной части окна. В следующем примере используется текущее расположение прокрутки и размеры недействительного региона для определения диапазона строк в недопустимом регионе для их отображения.

## <a name="example-of-scrolling-text"></a>Пример прокрутки текста

В следующем примере показана оконная процедура для окна, отображающего текст в клиентской области. В примере демонстрируется прокрутка текста в ответ на ввод из горизонтальной и вертикальной полос прокрутки.


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
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
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
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
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
    case WM_DESTROY :
        PostQuitMessage (0);
        return 0;
    }

    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование полос прокрутки](using-scroll-bars.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 