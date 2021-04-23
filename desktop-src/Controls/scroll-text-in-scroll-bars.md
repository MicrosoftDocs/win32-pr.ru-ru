---
title: Прокрутка текста
description: В этом разделе описываются изменения, которые можно внести в главное окно приложения, чтобы разрешить пользователю прокручивать текст.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891097"
---
# <a name="how-to-scroll-text"></a><span data-ttu-id="52106-103">Прокрутка текста</span><span class="sxs-lookup"><span data-stu-id="52106-103">How to Scroll Text</span></span>

<span data-ttu-id="52106-104">В этом разделе описываются изменения, которые можно внести в главное окно приложения, чтобы разрешить пользователю прокручивать текст.</span><span class="sxs-lookup"><span data-stu-id="52106-104">This section describes the changes you can make to an application's main window procedure to enable a user to scroll text.</span></span> <span data-ttu-id="52106-105">В примере в этом разделе создается и отображается массив текстовых строк, а также обрабатываются сообщения [**\_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) полосы прокрутки, чтобы пользователь мог прокручивать текст как по вертикали, так и по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="52106-105">The example in this section creates and displays an array of text strings, and processes [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) scroll bar messages so that the user can scroll text both vertically and horizontally.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="52106-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="52106-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="52106-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="52106-107">Technologies</span></span>

-   [<span data-ttu-id="52106-108">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="52106-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="52106-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="52106-109">Prerequisites</span></span>

-   <span data-ttu-id="52106-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="52106-110">C/C++</span></span>
-   <span data-ttu-id="52106-111">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="52106-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="52106-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="52106-112">Instructions</span></span>

### <a name="processing-the-wm_create-message"></a><span data-ttu-id="52106-113">Обработка сообщения о \_ создании WM</span><span class="sxs-lookup"><span data-stu-id="52106-113">Processing the WM\_CREATE Message</span></span>

<span data-ttu-id="52106-114">Единицы прокрутки обычно задаются при обработке сообщения о [**\_ создании WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="52106-114">Scrolling units are typically set while processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="52106-115">Удобно основывать единицы прокрутки по измерениям шрифта, связанного с контекстом устройства (DC) окна.</span><span class="sxs-lookup"><span data-stu-id="52106-115">It is convenient to base the scrolling units on the dimensions of the font associated with the window's device context (DC).</span></span> <span data-ttu-id="52106-116">Чтобы получить размеры шрифта для определенного контроллера домена, используйте функцию [**жеттекстметрикс**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) .</span><span class="sxs-lookup"><span data-stu-id="52106-116">To retrieve the font dimensions for a specific DC, use the [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) function.</span></span>

<span data-ttu-id="52106-117">В примере в этом разделе одна вертикальная единица прокрутки эквивалентна высоте ячейки символов, а также внешним ведущим.</span><span class="sxs-lookup"><span data-stu-id="52106-117">In the example in this section, one vertical scrolling unit is equivalent to the height of a character cell, plus external leading.</span></span> <span data-ttu-id="52106-118">Одна горизонтальная единица прокрутки эквивалентна средней ширине ячейки символов.</span><span class="sxs-lookup"><span data-stu-id="52106-118">One horizontal scrolling unit is equivalent to the average width of a character cell.</span></span> <span data-ttu-id="52106-119">Поэтому позиции горизонтальной прокрутки не соответствуют фактическим символам, если экранный шрифт не имеет фиксированной ширины.</span><span class="sxs-lookup"><span data-stu-id="52106-119">The horizontal scrolling positions, therefore, do not correspond to actual characters, unless the screen font is fixed-width.</span></span>

### <a name="processing-the-wm_size-message"></a><span data-ttu-id="52106-120">Обработка сообщения о \_ размере WM</span><span class="sxs-lookup"><span data-stu-id="52106-120">Processing the WM\_SIZE Message</span></span>

<span data-ttu-id="52106-121">При обработке сообщения [**о \_ размере WM**](/windows/desktop/winmsg/wm-size) удобно настроить диапазон прокрутки и расположение прокрутки, чтобы отразить размеры клиентской области, а также количество строк текста, которые будут отображены.</span><span class="sxs-lookup"><span data-stu-id="52106-121">When processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, it is convenient to adjust the scrolling range and scrolling position to reflect the dimensions of the client area as well as the number of lines of text that will be displayed.</span></span>

<span data-ttu-id="52106-122">Функция [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) задает минимальные и максимальные значения позиций, размер страницы и расположение прокрутки для полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="52106-122">The [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function sets the minimum and maximum position values, the page size, and the scrolling position for a scroll bar.</span></span>

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a><span data-ttu-id="52106-123">Обработка сообщений WM \_ HSCROLL и WM \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="52106-123">Processing the WM\_HSCROLL and WM\_VSCROLL Messages</span></span>

<span data-ttu-id="52106-124">Полоса прокрутки отправляет сообщения [**WM \_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) в оконную процедуру всякий раз, когда пользователь щелкает полосу прокрутки или перетаскивает ползунок.</span><span class="sxs-lookup"><span data-stu-id="52106-124">The scroll bar sends [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to the window procedure whenever the user clicks the scroll bar or drags the scroll box.</span></span> <span data-ttu-id="52106-125">Неупорядоченные слова **WM \_ VSCROLL** и **WM \_ HSCROLL** содержат код запроса, который указывает направление и величину действия прокрутки.</span><span class="sxs-lookup"><span data-stu-id="52106-125">The low-order words of **WM\_VSCROLL** and **WM\_HSCROLL** each contain a request code that indicates the direction and magnitude of the scrolling action.</span></span>

<span data-ttu-id="52106-126">При обработке сообщений [**WM \_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) проверяется код запроса полосы прокрутки, а шаг прокрутки вычисляется.</span><span class="sxs-lookup"><span data-stu-id="52106-126">When the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages are processed, the scroll bar request code is examined and the scrolling increment is calculated.</span></span> <span data-ttu-id="52106-127">После применения приращения к текущей положении прокрутки окно прокручивается до новой позицией с помощью функции [**скроллвиндовекс**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) , а расположение ползунка корректируется с помощью функции [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="52106-127">After the increment is applied to the current scrolling position, the window is scrolled to the new position by using the [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) function, and the position of the scroll box is adjusted by using the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span>

<span data-ttu-id="52106-128">После прокрутки окна часть его клиентской области становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="52106-128">After a window is scrolled, part of its client area is made invalid.</span></span> <span data-ttu-id="52106-129">Чтобы обеспечить обновление недопустимого региона, функция [**упдатевиндов**](/windows/desktop/api/winuser/nf-winuser-updatewindow) используется для создания сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="52106-129">To ensure that the invalid region is updated, the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function is used to generate a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

### <a name="processing-the-wm_paint-message"></a><span data-ttu-id="52106-130">Обработка сообщения WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="52106-130">Processing the WM\_PAINT Message</span></span>

<span data-ttu-id="52106-131">При обработке сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) удобно нарисовать строки текста, которые должны отображаться в недействительной части окна.</span><span class="sxs-lookup"><span data-stu-id="52106-131">When processing the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, it is convenient to draw the lines of text that you want to appear in the invalid portion of the window.</span></span> <span data-ttu-id="52106-132">В следующем примере используется текущее расположение прокрутки и размеры недействительного региона для определения диапазона строк в недопустимом регионе для их отображения.</span><span class="sxs-lookup"><span data-stu-id="52106-132">The following example uses the current scrolling position and the dimensions of the invalid region to determine the range of lines within the invalid region in order to display them.</span></span>

## <a name="example-of-scrolling-text"></a><span data-ttu-id="52106-133">Пример прокрутки текста</span><span class="sxs-lookup"><span data-stu-id="52106-133">Example of Scrolling Text</span></span>

<span data-ttu-id="52106-134">В следующем примере показана оконная процедура для окна, отображающего текст в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="52106-134">The following example is a window procedure for a window that displays text in its client area.</span></span> <span data-ttu-id="52106-135">В примере демонстрируется прокрутка текста в ответ на ввод из горизонтальной и вертикальной полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="52106-135">The example demonstrates how to scroll the text in response to input from the horizontal and vertical scroll bars.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="52106-136">См. также</span><span class="sxs-lookup"><span data-stu-id="52106-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52106-137">Использование полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="52106-137">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="52106-138">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="52106-138">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 