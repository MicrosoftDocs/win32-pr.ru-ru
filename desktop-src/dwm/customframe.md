---
title: Настраиваемая рамка окна с помощью DWM
description: В этом разделе показано, как использовать интерфейсы API диспетчер окон рабочего стола (DWM) для создания пользовательских рамок окон для приложения.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Диспетчер окон рабочего стола (DWM), пользовательские рамки окон
- DWM (диспетчер окон рабочего стола), пользовательские рамки окон
- Пользовательские рамки окон
- Удаление стандартных кадров
- Расширение клиентских рамок
- Диспетчер окон рабочего стола (DWM), расширение кадров клиента
- DWM (диспетчер окон рабочего стола), расширение кадров клиента
- Диспетчер окон рабочего стола (DWM), удаление стандартных кадров
- DWM (диспетчер окон рабочего стола), удаление стандартных кадров
- Диспетчер окон рабочего стола (DWM), рисование в расширенных кадрах
- DWM (диспетчер окон рабочего стола), рисование в расширенных кадрах
- Рисование в расширенных кадрах
- проверка нажатия
- Диспетчер окон рабочего стола (DWM), проверка нажатия
- DWM (диспетчер окон рабочего стола), проверка нажатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070589"
---
# <a name="custom-window-frame-using-dwm"></a>Настраиваемая рамка окна с помощью DWM

В этом разделе показано, как использовать интерфейсы API диспетчер окон рабочего стола (DWM) для создания пользовательских рамок окон для приложения.

-   [Введение](#introduction)
-   [Расширение клиентского фрейма](#extending-the-client-frame)
-   [Удаление стандартного кадра](#removing-the-standard-frame)
-   [Рисование в окне расширенного фрейма](#drawing-in-the-extended-frame-window)
-   [Включение проверки нажатия для пользовательского кадра](#enabling-hit-testing-for-the-custom-frame)
-   [Приложение а. Процедура примера окна](#appendix-a-sample-window-procedure)
-   [Приложение б. Рисование заголовка подписи](#appendix-b-painting-the-caption-title)
-   [Приложение в. функция Хиттестнка](#appendix-c-hittestnca-function)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

В Windows Vista и более поздних версиях внешний вид неклиентской области окон приложений (строки заголовка, значка, границы окна и кнопки заголовка) управляется DWM. С помощью интерфейсов API DWM можно изменить способ отрисовки кадра окон DWM.

Одной из функций API DWM является возможность расширения фрейма приложения в клиентскую область. Это позволяет интегрировать элемент пользовательского интерфейса клиента (например, панель инструментов) в рамку, предоставляя пользовательскому интерфейсу возможность управлять более заметным местом в пользовательском интерфейсе приложения. Например, Windows Internet Explorer 7 в Windows Vista интегрирует панель навигации в рамку окна, расширяя верхнюю часть рамки, как показано на следующем снимке экрана.

![панель навигации, интегрированная в рамку окна.](images/ie7-extendedborder-boxed.png)

Возможность расширения рамки окна также позволяет создавать пользовательские фреймы, сохраняя внешний вид окна. Например, Microsoft Office Word 2007 рисует кнопку Office и панель быстрого доступа внутри пользовательского фрейма, предоставляя стандартные кнопки сворачивания, развертывания и закрытия, как показано на следующем снимке экрана.

![Кнопка Office и панель быстрого доступа в Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Расширение клиентского фрейма

Функциональные возможности расширения рамки в клиентской области предоставляются функцией [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Чтобы расширить рамку, передайте маркер целевого окна вместе со значениями отступов полей в **DwmExtendFrameIntoClientArea**. Значения отступа полей определяют, насколько далеко можно расширять рамку на четырех сторонах окна.

В следующем коде показано использование [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) для расширения рамки.


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



Обратите внимание, что расширение Frame выполняется в [**сообщении \_ активации WM**](/windows/desktop/inputdev/wm-activate) , а не в сообщении [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) . Это гарантирует, что расширение кадра будет правильно обрабатываться, если размер окна по умолчанию и когда он развернут.

На следующем рисунке показана стандартная рамка окна (слева) и та же самая Расширенная рамка окна (справа). Фрейм расширяется с помощью предыдущего примера кода и по умолчанию Microsoft Visual Studio [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) фон ( \_ окно цвета + 1).

![снимок экрана со стандартной (левой) и расширенной рамкой (справа) с белым фоном](images/white-sidebyside.png)

Визуальное различие между этими двумя окнами очень незаметно. Единственное различие между ними заключается в том, что тонкая черная граница области клиента в окне слева отсутствует в окне справа. Причиной этой отсутствующей границы является то, что она включена в расширенный кадр, а остальная часть клиентской области — нет. Для отображения расширенных кадров области, лежащие в основе каждой стороны расширенного кадра, должны иметь точечные данные с альфа-значением 0. Черная граница вокруг области клиента содержит данные пикселей, в которых все цветовые значения (красный, зеленый, синий и альфа) имеют значение 0. В остальной части фона значение альфа не равно 0, поэтому остальная часть расширенного кадра не отображается.

Самый простой способ убедиться в том, что расширенные кадры видимы, — это сделать весь клиентский регион черным. Для этого инициализируйте элемент *хбрбаккграунд* структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) или [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) в дескрипторе черной \_ кисти. На следующем рисунке показан один и тот же стандартный фрейм (слева) и расширенный фрейм (справа), показанные ранее. Однако на этот раз для *хбрбаккграунд* ЗАДАН маркер черной кисти, \_ полученный из функции [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .

![снимок экрана: Стандартная (слева) и расширенная рамка (справа) с черным фоном](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Удаление стандартного кадра

После того как вы расширили фрейм приложения и сделали его видимым, можно удалить стандартный фрейм. Удаление стандартного кадра позволяет управлять шириной каждой стороны рамки, а не просто расширением стандартного фрейма.

Чтобы удалить стандартный фрейм окна, необходимо выполнить обработку сообщения [**WM \_ нккалксизе**](/windows/desktop/winmsg/wm-nccalcsize) , в частности, если его значение *wParam* равно **true** , а возвращаемое значение равно 0. При этом приложение использует всю область окна в качестве клиентской области, удаляя стандартный фрейм.

Результаты обработки сообщения [**WM \_ нккалксизе**](/windows/desktop/winmsg/wm-nccalcsize) не видны, пока не потребуется изменить размер региона клиента. До этого времени начальное представление окна отображается со стандартным фреймом и расширенными границами. Чтобы преодолеть это, необходимо либо изменить размер окна, либо выполнить действие, запускающее сообщение **WM \_ нккалксизе** во время создания окна. Это можно сделать с помощью функции [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) , чтобы переместить окно и изменить его размер. В следующем примере кода демонстрируется вызов **SetWindowPos** , который вызывает отправку сообщения **WM \_ нккалксизе** с помощью атрибутов прямоугольника окна и \_ флага СВП фрамечанжед.


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



На следующем рисунке показан стандартный фрейм (слева) и новый расширенный кадр без стандартного кадра (справа).

![снимок экрана: Стандартный кадр (слева) и настраиваемый кадр (справа)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Рисование в окне расширенного фрейма

При удалении стандартного кадра теряется автоматическое рисование значка и названия приложения. Чтобы добавить их обратно в приложение, необходимо нарисовать их самостоятельно. Для этого сначала просмотрите изменения, которые произошли в клиентской области.

После удаления стандартного кадра клиентская область теперь состоит из всего окна, включая расширенный кадр. Сюда входит область, в которой рисуются кнопки заголовка. В следующем параллельном сравнении клиентская область для стандартного кадра и пользовательского расширенного кадра выделяется красным цветом. Область клиента для стандартного окна фрейма (слева) — это черная область. В расширенном окне фрейма (справа) клиентская область — это все окно.

![снимок экрана с красной выделенной областью клиента на стандартном и настраиваемом кадре](images/clientarea-sidebyside.png)

Так как все окно является клиентской областью, можно просто нарисовать нужные объекты в расширенном кадре. Чтобы добавить заголовок в приложение, просто выведите текст в соответствующем регионе. На следующем рисунке показан текст темы, нарисованный в пользовательском фрейме заголовка. Заголовок рисуется с помощью функции [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) . Чтобы просмотреть код, рисующий заголовок, см. [приложение б. закраска заголовка](#appendix-b-painting-the-caption-title).

![снимок экрана с пользовательской рамкой с заголовком](images/custom-caption-title.png)

> [!Note]  
> При рисовании в пользовательском фрейме Будьте внимательны при размещении элементов управления пользовательского интерфейса. Так как все окно является регионом клиента, необходимо настроить размещение элементов управления пользовательского интерфейса для каждой ширины кадра, если они не должны отображаться в или в расширенном фрейме.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Включение проверки нажатия для пользовательского кадра

Побочным результатом удаления стандартного фрейма является утрата поведения изменения размера и перемещения по умолчанию. Чтобы приложение правильно эмулировать поведение стандартного окна, необходимо реализовать логику обработки проверки нажатия кнопки "заголовок" и изменения размера или перемещения кадра.

Для проверки нажатия кнопки субтитров DWM предоставляет функцию [**двмдефвиндовпрок**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) . Для правильной проверки нажатия кнопок субтитров в сценариях с пользовательскими кадрами сообщения должны быть передаваться в **двмдефвиндовпрок** для обработки. **Двмдефвиндовпрок** возвращает **значение true** , если сообщение обрабатывается, и **значение false** в противном случае. Если сообщение не обрабатывается **двмдефвиндовпрок**, приложение должно обработать само сообщение или передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Для изменения размера и перемещения фрейма приложение должно предоставить логику проверки попадания и обработку сообщений проверки нажатия кадра. Сообщения проверки нажатия фрейма отправляются вам через сообщение [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) , даже если приложение создает пользовательский фрейм без стандартного кадра. Следующий код демонстрирует обработку сообщения **WM \_ нчиттест** , когда [**двмдефвиндовпрок**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) не обрабатывает его. Код вызываемой `HitTestNCA` функции см. в [приложении C: хиттестнка Function](#appendix-c-hittestnca-function).


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a>Приложение а. Процедура примера окна

В следующем примере кода демонстрируется процедура окна и вспомогательные функции, которые используются для создания пользовательского приложения с фреймами.


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a>Приложение б. Рисование заголовка подписи

В следующем коде показано, как закрасить заголовок заголовка в расширенном кадре. Эта функция должна вызываться из вызовов [**бегинпаинт**](/windows/desktop/api/winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/winuser/nf-winuser-endpaint) .


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a>Приложение в. функция Хиттестнка

В следующем коде показана `HitTestNCA` функция, используемая при [проверке нажатия для пользовательского фрейма](#enabling-hit-testing-for-the-custom-frame). Эта функция обрабатывает логику проверки попадания для [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) , когда [**двмдефвиндовпрок**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) не обрабатывает сообщение.


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о диспетчере окон рабочего стола](dwm-overview.md)
</dt> </dl>

 

 