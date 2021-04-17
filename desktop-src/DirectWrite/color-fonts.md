---
title: Шрифты цвета
description: В этом разделе описываются цветовые шрифты, их поддержка в DirectWrite и Direct2D, а также способы их использования в приложении.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "104556757"
---
# <a name="color-fonts"></a>Шрифты цвета

В этом разделе описываются цветовые шрифты, их поддержка в DirectWrite и Direct2D, а также способы их использования в приложении.

Этот документ содержит следующие компоненты:

-   [Что такое цветовые шрифты?](#what-are-color-fonts)
-   [Зачем использовать цветные шрифты?](#why-use-color-fonts)
-   [Какие цвета шрифты поддерживаются в Windows?](#what-kinds-of-color-fonts-does-windows-support)
-   [Использование цветовых шрифтов](#using-color-fonts)
    -   [Использование цветовых шрифтов в приложении XAML](#using-color-fonts-in-a-xaml-app)
    -   [Использование цветовых шрифтов в Microsoft ребро](#using-color-fonts-in-microsoft-edge)
    -   [Использование цветовых шрифтов с DirectWrite и Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Использование цветовых шрифтов с Win2D](#using-color-fonts-with-win2d)
-   [См. также](#related-topics)

## <a name="what-are-color-fonts"></a>Что такое цветовые шрифты?

Цветовые шрифты, также называемые многоцветными шрифтами или цветовыми шрифтами, — это технология шрифтов, позволяющая проектировщикам шрифтов использовать несколько цветов в каждом глифе. Цветовые шрифты позволяют использовать многоцветные текстовые сценарии в приложениях и веб-сайтах с меньшим объемом кода и более устойчивой поддержкой операционной системы, чем специальные методики, реализованные над системой визуализации текста.

Шрифты, которые, скорее всего, хорошо знакомы, не являются цветными шрифтами. Эти шрифты определяют только форму глифов, которые они содержат, с помощью векторных контуров или монохромных растров. Во время рисования модуль обработки текста заполняет фигуру глифов, используя один цвет (цвет шрифта), заданный приложением или документом, который готовится к просмотру. Цветовые шрифты, с другой стороны, содержат сведения о цвете в дополнение к сведениям о фигуре. Некоторые подходы позволяют разработчикам шрифтов предлагать несколько цветовых палитр, давая цветному шрифту гибкость.

В следующем примере показан глиф из цветового шрифта Segoe UI эмодзи. Глиф отображается в виде монохромного изображения слева, а цвет — справа.

![Показывает односторонние глифы, левый глиф, отображаемый в монохромном режиме, право на цветном шрифте Segoe U I эмодзи.](images/color-font-cat.png)

Цветовые шрифты обычно включают резервные сведения для платформ, которые не поддерживают цветовые шрифты, или для сценариев, в которых отключена функция цвета. На этих платформах цветные шрифты подготавливаются к просмотру как обычные монохромные шрифты.

## <a name="why-use-color-fonts"></a>Зачем использовать цветные шрифты?

Исторически разработчики и разработчики использовали разнообразные методы для достижения многоцветного текста. Например, веб-сайты часто используют растровые изображения вместо текста для вывода форматированных заголовков. Такой подход обеспечивает художественную гибкость, но растровая графика не масштабируется для всех размеров, а также не предоставляет такие же специальные возможности, как и реальный текст. Другой распространенной методикой является наложение нескольких монохромных шрифтов различными цветами шрифта, но для управления им обычно требуется дополнительный код макета.

Цветовые шрифты предлагают способ достижения этих визуальных эффектов со всей простотой и функциональными возможностями обычных шрифтов. Текст, отображаемый в цветном шрифте, совпадает с другим текстом: он может быть скопирован и вставлен, он может быть проанализирован средствами специальных возможностей и т. д.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Какие цвета шрифты поддерживаются в Windows?

[Спецификация OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) определяет несколько способов внедрения информации о цвете в шрифт. Начиная с годовщины Windows 10, DirectWrite и Direct2D (и построенные на них платформы Windows) поддерживают все эти подходы. Они представлены в следующей таблице:



| Метод                                                                                                                        | Описание                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Колр](/typography/opentype/spec/colr) / [Кпал](/typography/opentype/spec/cpal) таблицы | Использует слои цветных векторов, фигуры которых определяются таким же образом, как контуры глифов одного цвета. **Примечание.** Поддерживается начиная с Windows 8.1. <br/>                                                                                                                                                 |
| Таблица [SVG](/typography/opentype/spec/svg)                                                                 | Использует векторные изображения, созданные в масштабируемом векторном графическом формате. **Примечание.** Начиная с годовщины Windows 10, DirectWrite поддерживает подмножество полных спецификаций SVG. Не все содержимое SVG гарантированно отображается в шрифте OpenType SVG. Дополнительные сведения см. в разделе [Поддержка SVG](../direct2d/svg-support.md) . <br/> |
| [Кбдт](/typography/opentype/spec/cbdt) / [Кблк](/typography/opentype/spec/cblc) таблицы | Использует встроенные цветные растровые изображения.                                                                                                                                                                                                                                                                                |
| Таблица [сбикс](/typography/opentype/spec/sbix)                                                               | Использует встроенные цветные растровые изображения.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Использование цветовых шрифтов

С точки зрения пользователя цветовые шрифты являются просто шрифтами. Например, они обычно устанавливаются и удаляются из системы так же, как монохромные шрифты, и подготавливаются к просмотру как обычный, выбираемый текст.

С точки зрения разработчика, цветовые шрифты обычно используются так же, как монохромные шрифты. В платформах XAML и Microsoft ребра можно использовать цветовые шрифты так же, как обычные шрифты, и по умолчанию текст будет отображаться в цвете. Однако если приложение напрямую вызывает API Direct2D (или Win2D API) для отрисовки текста, оно должно явно запрашивать визуализацию цветового шрифта.

### <a name="using-color-fonts-in-a-xaml-app"></a>Использование цветовых шрифтов в приложении XAML

Текстовые элементы платформы XAML (такие как [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [Ричедитбокс](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)и [фонтикон](/uwp/api/windows.ui.xaml.controls.fonticon)) поддерживают цветовые шрифты по умолчанию. Просто создайте стиль текста с помощью цветового шрифта, и все глифы цвета будут подготавливаться к просмотру цветом. В следующем примере кода показан один из способов стиля элемента управления TextBlock с помощью цветового шрифта, упакованного в приложение. Тот же метод применяется к обычным шрифтам.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Если вы никогда не хотите, чтобы элемент текста XAML отображал многоцветный текст, установите для его свойства [исколорфонтенабледпроперти](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) значение false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Использование цветовых шрифтов в Microsoft ребро

Цветовые шрифты отображаются по умолчанию на веб-сайтах и веб-приложениях, работающих в Microsoft погранично, включая элемент управления XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) . Просто используйте HTML и CSS для стиля текста с помощью цветового шрифта, а цветовые глифы будут подготавливаться к просмотру цветом.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Использование цветовых шрифтов с DirectWrite и Direct2D

Приложение может использовать методы рисования текста более высокого уровня Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) и [**дравтекстлайаут**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) или использовать методы более низкого уровня для прорисовки запуска глифов напрямую. В любом случае приложение требует изменения кода, чтобы правильно обрабатывались глифы цвета. Если приложение использует API-интерфейсы Direct2D **DrawText** и **дравтекстлайаут** , обратите внимание, что по умолчанию не отображаются глифы цвета. Это позволяет избежать непредвиденных изменений в работе приложений для отрисовки текста, разработанных до цветной поддержки цветовых шрифтов.

Чтобы принять участие в визуализации цветовых глифов, передайте параметр [**D2D1 \_ Draw \_ Text (включить параметры \_ \_ \_ цветового \_ шрифта**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) ) в метод Drawing. В следующем примере кода показано, как вызвать метод Direct2D s DrawText для отображения строки в цветном шрифте:


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



Если приложение использует интерфейсы API более низкого уровня для обработки глифов напрямую, оно будет продолжать работать при наличии цветовых шрифтов, но не сможет рисовать цветовые глифы без дополнительной логики.

Чтобы правильно обрабатывались цветовые глифы, приложение должно выполнить следующие действия:

1.  Передайте сведения о запуске глифа в [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), а также параметр [**\_ \_ \_ форматов изображения глифа дврите**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) , указывающий типы цветовых глифов, которые приложение подготовлено к обработке. Если имеются любые цветовые глифы (на основе шрифта и запрошенных **\_ \_ \_ форматов изображения глифа Дврите**), то DirectWrite будет разделять основной глиф, выполняемый в отдельном цветном глифе, к которому можно получить доступ с помощью возвращенного объекта [**идвритеколорглифруненумератор**](idwritecolorglyphrunenumerator.md) на шаге 4.
2.  Проверьте значение HRESULT, возвращаемое функцией [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) , чтобы определить, были ли обнаружены какие — глифы цвета. **Значение HRESULT** для **дврите \_ E \_** указывает, что соответствующий цвет глифа цвета не выполняется.
3.  Если [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) не запустил цветовой глиф (путем возвращения **дврите \_ E \_ Color**), то весь фрагмент глифа рассматривается как монохромный, и приложение должно нарисовать его по желанию (например, с помощью [**ID2D1DeviceContext::D равглифрун**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Если [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) сообщает о наличии цветового глифа, приложение должно игнорировать выполнение основного глифа, а вместо этого использовать число запусков глифов цвета, возвращенных транслатеколорглифрун. Для этого выполните итерацию возвращенного объекта [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) , извлекая каждый цветовой глиф и нарисовав его в соответствии с форматом изображения глифа (например, можно использовать [**дравколорбитмапглифрун**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) и [**дравсвгглифрун**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) для рисования цветных глифов и глифов SVG соответственно).

В следующем примере кода показана общая структура этой процедуры:


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>Использование цветовых шрифтов с Win2D

Как и в API-интерфейсах Direct2D, Win2D s, по умолчанию не отображаются цветовые глифы. Чтобы принять участие в визуализации цветовых глифов, установите флаг параметров [енаблеколорфонт](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) в объекте текстового формата, который приложение передает в метод рисования текста. В следующем примере кода показано, как визуализировать строку в цветовой шрифт с помощью Win2D:


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>См. также

[Образец цветового глифа DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Интерфейс IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**Метод IDWriteFactory4:: Транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4: метод:D Равтекст**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

