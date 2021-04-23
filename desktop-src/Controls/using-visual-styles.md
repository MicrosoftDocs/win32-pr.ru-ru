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
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="3d3c2-103">Использование стилей оформления с пользовательскими и Owner-Drawn элементами управления</span><span class="sxs-lookup"><span data-stu-id="3d3c2-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="3d3c2-104">В этом разделе описывается использование API визуальных стилей для применения визуальных стилей к пользовательским элементам управления или рисуемым владельцем элементам управления.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="3d3c2-105">Рисование элементов управления с помощью визуальных стилей</span><span class="sxs-lookup"><span data-stu-id="3d3c2-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="3d3c2-106">Реагирование на изменения темы</span><span class="sxs-lookup"><span data-stu-id="3d3c2-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="3d3c2-107">См. также</span><span class="sxs-lookup"><span data-stu-id="3d3c2-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="3d3c2-108">Рисование элементов управления с помощью визуальных стилей</span><span class="sxs-lookup"><span data-stu-id="3d3c2-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="3d3c2-109">Визуальные стили поддерживаются ComCtrl32.dll версии 6 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="3d3c2-110">Если приложение настроено для использования ComCtrl32.dll версии 6 и более поздних версий и, если эта версия доступна в системе, текущие стили оформления автоматически применяются ко всем общим элементам управления в приложении.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="3d3c2-111">Однако текущие стили оформления не применяются автоматически к пользовательским элементам управления или рисуемым владельцем элементам управления.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="3d3c2-112">Приложение должно включать код, который проверяет, доступны ли стили оформления, и, если это так, использует API визуальных стилей для применения выбранных в данный момент стилей оформления к пользовательским и рисуемым пользователем элементам управления.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="3d3c2-113">Чтобы проверить, доступны ли стили оформления, вызовите функцию [**исаппсемед**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) .</span><span class="sxs-lookup"><span data-stu-id="3d3c2-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="3d3c2-114">Если визуальные стили недоступны, для рисования элемента управления используйте резервный код.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="3d3c2-115">Если доступны стили оформления, можно использовать функции визуальных стилей, такие как [**дравсеметекст**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , для отрисовки элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="3d3c2-116">Обратите внимание, что [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) позволяет настраивать внешний вид текста, сохраняя некоторые свойства шрифта темы при изменении других.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="3d3c2-117">**Рисование элемента управления в текущем визуальном стиле**</span><span class="sxs-lookup"><span data-stu-id="3d3c2-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="3d3c2-118">Вызовите [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), передав *HWND* элемента управления, к которому нужно применить стили оформления, и список классов, описывающий тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="3d3c2-119">Классы определяются в Vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="3d3c2-120">**Опенсемедата** ВОЗВРАЩАЕТ маркер хсеме, но если Диспетчер визуальных стилей отключен или текущий визуальный стиль не предоставляет определенные сведения для данного элемента управления, функция возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="3d3c2-121">Если возвращаемое значение равно **null**, используйте функции рисования, не связанные с визуальным стилем.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="3d3c2-122">Чтобы нарисовать фон элемента управления, вызовите [**дравсемебаккграунд**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) или [**дравсемебаккграундекс**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span><span class="sxs-lookup"><span data-stu-id="3d3c2-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="3d3c2-123">Чтобы определить расположение прямоугольника содержимого, вызовите [**жетсемебаккграундконтентрект**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="3d3c2-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="3d3c2-124">Для отрисовки текста используйте либо [**дравсеметекст**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , либо [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), на основе координат прямоугольника, возвращаемого [**жетсемебаккграундконтентрект**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="3d3c2-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="3d3c2-125">Эти функции могут отображать текст в шрифте темы для указанной части элемента управления и ее состояния, а также в шрифте, выбранном в контексте устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="3d3c2-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="3d3c2-126">Когда элемент управления получает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) , вызовите [**клосесемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) , чтобы освободить маркер темы, который был возвращен при вызове [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="3d3c2-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="3d3c2-127">В следующем примере кода демонстрируется один из способов рисования элемента управления "Кнопка" в текущем визуальном стиле.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


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





<span data-ttu-id="3d3c2-128">Следующий пример кода находится в обработчике сообщений [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) для элемента управления "Кнопка" с подклассом.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="3d3c2-129">Текст элемента управления отображается в шрифте визуальных стилей, но цвет определяется приложением в зависимости от состояния элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


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



<span data-ttu-id="3d3c2-130">Можно использовать части из других элементов управления и визуализировать каждую часть отдельно.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="3d3c2-131">Например, для элемента управления Calendar, состоящего из сетки, каждый квадрат, сформированный сеткой, можно рассматривать как кнопку на панели инструментов, получая маркер темы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3d3c2-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="3d3c2-132">Можно сочетать и сопоставлять управляющие элементы, вызывая [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) несколько раз для заданного элемента управления и используя соответствующий маркер темы для рисования различных частей.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="3d3c2-133">Однако в некоторых визуальных стилях некоторые части могут быть несовместимы с другими частями.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="3d3c2-134">Другим подходом к визуализации элементов управления в активном визуальном стиле является использование системных цветов.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="3d3c2-135">Например, можно использовать системные цвета для установки цвета текста при вызове функции [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="3d3c2-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="3d3c2-136">Большинство системных цветов задаются при применении файла визуального стиля.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="3d3c2-137">Реагирование на изменения темы</span><span class="sxs-lookup"><span data-stu-id="3d3c2-137">Responding to Theme Changes</span></span>

<span data-ttu-id="3d3c2-138">Когда элемент управления получает сообщение [**WM \_ семечанжед**](/windows/desktop/winmsg/wm-themechanged) и удерживает глобальный маркер для темы, он должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3d3c2-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="3d3c2-139">Вызовите [**клосесемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) , чтобы закрыть существующий маркер темы.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="3d3c2-140">Вызовите [**опенсемедата**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) , чтобы получить маркер темы для вновь загруженного визуального стиля.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="3d3c2-141">В следующем примере показаны два вызова.</span><span class="sxs-lookup"><span data-stu-id="3d3c2-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="3d3c2-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3d3c2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d3c2-143">Включение стилей оформления</span><span class="sxs-lookup"><span data-stu-id="3d3c2-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="3d3c2-144">Стили оформления</span><span class="sxs-lookup"><span data-stu-id="3d3c2-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 