---
title: Использование стилей оформления с пользовательскими и Owner-Drawn элементами управления
description: В этом разделе описывается использование API визуальных стилей для применения визуальных стилей к пользовательским элементам управления или рисуемым владельцем элементам управления.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134670"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>Использование стилей оформления с пользовательскими и Owner-Drawn элементами управления

В этом разделе описывается использование API визуальных стилей для применения визуальных стилей к пользовательским элементам управления или рисуемым владельцем элементам управления.

-   [Рисование элементов управления с помощью визуальных стилей](#drawing-controls-with-visual-styles)
-   [Реагирование на изменения темы](#responding-to-theme-changes)
-   [См. также](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>Рисование элементов управления с помощью визуальных стилей

Визуальные стили поддерживаются ComCtrl32.dll версии 6 и более поздних. Если приложение настроено для использования ComCtrl32.dll версии 6 и более поздних версий и, если эта версия доступна в системе, текущие стили оформления автоматически применяются ко всем общим элементам управления в приложении. Однако текущие стили оформления не применяются автоматически к пользовательским элементам управления или рисуемым владельцем элементам управления. Приложение должно включать код, который проверяет, доступны ли стили оформления, и, если это так, использует API визуальных стилей для применения выбранных в данный момент стилей оформления к пользовательским и рисуемым пользователем элементам управления.

Чтобы проверить, доступны ли стили оформления, вызовите функцию [**исаппсемед**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) . Если визуальные стили недоступны, для рисования элемента управления используйте резервный код.

Если доступны стили оформления, можно использовать функции визуальных стилей, такие как [**дравсеметекст**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , для отрисовки элемента управления. Обратите внимание, что [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) позволяет настраивать внешний вид текста, сохраняя некоторые свойства шрифта темы при изменении других.

**Рисование элемента управления в текущем визуальном стиле**

1.  Вызовите [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), передав *HWND* элемента управления, к которому нужно применить стили оформления, и список классов, описывающий тип элемента управления. Классы определяются в Vssym32. h. **Опенсемедата** ВОЗВРАЩАЕТ маркер хсеме, но если Диспетчер визуальных стилей отключен или текущий визуальный стиль не предоставляет определенные сведения для данного элемента управления, функция возвращает **значение NULL**. Если возвращаемое значение равно **null**, используйте функции рисования, не связанные с визуальным стилем.
2.  Чтобы нарисовать фон элемента управления, вызовите [**дравсемебаккграунд**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) или [**дравсемебаккграундекс**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).
3.  Чтобы определить расположение прямоугольника содержимого, вызовите [**жетсемебаккграундконтентрект**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).
4.  Для отрисовки текста используйте либо [**дравсеметекст**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , либо [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), на основе координат прямоугольника, возвращаемого [**жетсемебаккграундконтентрект**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect). Эти функции могут отображать текст в шрифте темы для указанной части элемента управления и ее состояния, а также в шрифте, выбранном в контексте устройства (DC).
5.  Когда элемент управления получает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) , вызовите [**клосесемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) , чтобы освободить маркер темы, который был возвращен при вызове [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).

В следующем примере кода демонстрируется один из способов рисования элемента управления "Кнопка" в текущем визуальном стиле.


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





Следующий пример кода находится в обработчике сообщений [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) для элемента управления "Кнопка" с подклассом. Текст элемента управления отображается в шрифте визуальных стилей, но цвет определяется приложением в зависимости от состояния элемента управления.


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



Можно использовать части из других элементов управления и визуализировать каждую часть отдельно. Например, для элемента управления Calendar, состоящего из сетки, каждый квадрат, сформированный сеткой, можно рассматривать как кнопку на панели инструментов, получая маркер темы следующим образом:


```C++
OpenThemeData(hwnd, L"Toolbar");
```



Можно сочетать и сопоставлять управляющие элементы, вызывая [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) несколько раз для заданного элемента управления и используя соответствующий маркер темы для рисования различных частей. Однако в некоторых визуальных стилях некоторые части могут быть несовместимы с другими частями.

Другим подходом к визуализации элементов управления в активном визуальном стиле является использование системных цветов. Например, можно использовать системные цвета для установки цвета текста при вызове функции [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) . Большинство системных цветов задаются при применении файла визуального стиля.

## <a name="responding-to-theme-changes"></a>Реагирование на изменения темы

Когда элемент управления получает сообщение [**WM \_ семечанжед**](/windows/desktop/winmsg/wm-themechanged) и удерживает глобальный маркер для темы, он должен выполнить следующие действия:

-   Вызовите [**клосесемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) , чтобы закрыть существующий маркер темы.
-   Вызовите [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) , чтобы получить маркер темы для вновь загруженного визуального стиля.

В следующем примере показаны два вызова.


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Включение стилей оформления](cookbook-overview.md)
</dt> <dt>

[Стили оформления](themes-overview.md)
</dt> </dl>

 

 