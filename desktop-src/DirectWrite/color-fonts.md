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
# <a name="color-fonts"></a><span data-ttu-id="bd6a6-103">Шрифты цвета</span><span class="sxs-lookup"><span data-stu-id="bd6a6-103">Color Fonts</span></span>

<span data-ttu-id="bd6a6-104">В этом разделе описываются цветовые шрифты, их поддержка в DirectWrite и Direct2D, а также способы их использования в приложении.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="bd6a6-105">Этот документ содержит следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="bd6a6-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="bd6a6-106">Что такое цветовые шрифты?</span><span class="sxs-lookup"><span data-stu-id="bd6a6-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="bd6a6-107">Зачем использовать цветные шрифты?</span><span class="sxs-lookup"><span data-stu-id="bd6a6-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="bd6a6-108">Какие цвета шрифты поддерживаются в Windows?</span><span class="sxs-lookup"><span data-stu-id="bd6a6-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="bd6a6-109">Использование цветовых шрифтов</span><span class="sxs-lookup"><span data-stu-id="bd6a6-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="bd6a6-110">Использование цветовых шрифтов в приложении XAML</span><span class="sxs-lookup"><span data-stu-id="bd6a6-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="bd6a6-111">Использование цветовых шрифтов в Microsoft ребро</span><span class="sxs-lookup"><span data-stu-id="bd6a6-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="bd6a6-112">Использование цветовых шрифтов с DirectWrite и Direct2D</span><span class="sxs-lookup"><span data-stu-id="bd6a6-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="bd6a6-113">Использование цветовых шрифтов с Win2D</span><span class="sxs-lookup"><span data-stu-id="bd6a6-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="bd6a6-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bd6a6-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="bd6a6-115">Что такое цветовые шрифты?</span><span class="sxs-lookup"><span data-stu-id="bd6a6-115">What are color fonts?</span></span>

<span data-ttu-id="bd6a6-116">Цветовые шрифты, также называемые многоцветными шрифтами или цветовыми шрифтами, — это технология шрифтов, позволяющая проектировщикам шрифтов использовать несколько цветов в каждом глифе.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="bd6a6-117">Цветовые шрифты позволяют использовать многоцветные текстовые сценарии в приложениях и веб-сайтах с меньшим объемом кода и более устойчивой поддержкой операционной системы, чем специальные методики, реализованные над системой визуализации текста.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="bd6a6-118">Шрифты, которые, скорее всего, хорошо знакомы, не являются цветными шрифтами.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="bd6a6-119">Эти шрифты определяют только форму глифов, которые они содержат, с помощью векторных контуров или монохромных растров.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="bd6a6-120">Во время рисования модуль обработки текста заполняет фигуру глифов, используя один цвет (цвет шрифта), заданный приложением или документом, который готовится к просмотру.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="bd6a6-121">Цветовые шрифты, с другой стороны, содержат сведения о цвете в дополнение к сведениям о фигуре.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="bd6a6-122">Некоторые подходы позволяют разработчикам шрифтов предлагать несколько цветовых палитр, давая цветному шрифту гибкость.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="bd6a6-123">В следующем примере показан глиф из цветового шрифта Segoe UI эмодзи.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="bd6a6-124">Глиф отображается в виде монохромного изображения слева, а цвет — справа.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![Показывает односторонние глифы, левый глиф, отображаемый в монохромном режиме, право на цветном шрифте Segoe U I эмодзи.](images/color-font-cat.png)

<span data-ttu-id="bd6a6-126">Цветовые шрифты обычно включают резервные сведения для платформ, которые не поддерживают цветовые шрифты, или для сценариев, в которых отключена функция цвета.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="bd6a6-127">На этих платформах цветные шрифты подготавливаются к просмотру как обычные монохромные шрифты.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="bd6a6-128">Зачем использовать цветные шрифты?</span><span class="sxs-lookup"><span data-stu-id="bd6a6-128">Why use color fonts?</span></span>

<span data-ttu-id="bd6a6-129">Исторически разработчики и разработчики использовали разнообразные методы для достижения многоцветного текста.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="bd6a6-130">Например, веб-сайты часто используют растровые изображения вместо текста для вывода форматированных заголовков.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="bd6a6-131">Такой подход обеспечивает художественную гибкость, но растровая графика не масштабируется для всех размеров, а также не предоставляет такие же специальные возможности, как и реальный текст.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="bd6a6-132">Другой распространенной методикой является наложение нескольких монохромных шрифтов различными цветами шрифта, но для управления им обычно требуется дополнительный код макета.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="bd6a6-133">Цветовые шрифты предлагают способ достижения этих визуальных эффектов со всей простотой и функциональными возможностями обычных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="bd6a6-134">Текст, отображаемый в цветном шрифте, совпадает с другим текстом: он может быть скопирован и вставлен, он может быть проанализирован средствами специальных возможностей и т. д.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="bd6a6-135">Какие цвета шрифты поддерживаются в Windows?</span><span class="sxs-lookup"><span data-stu-id="bd6a6-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="bd6a6-136">[Спецификация OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) определяет несколько способов внедрения информации о цвете в шрифт.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="bd6a6-137">Начиная с годовщины Windows 10, DirectWrite и Direct2D (и построенные на них платформы Windows) поддерживают все эти подходы.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="bd6a6-138">Они представлены в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="bd6a6-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="bd6a6-139">Метод</span><span class="sxs-lookup"><span data-stu-id="bd6a6-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="bd6a6-140">Описание</span><span class="sxs-lookup"><span data-stu-id="bd6a6-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6a6-141">[Колр](/typography/opentype/spec/colr) / [Кпал](/typography/opentype/spec/cpal) таблицы</span><span class="sxs-lookup"><span data-stu-id="bd6a6-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="bd6a6-142">Использует слои цветных векторов, фигуры которых определяются таким же образом, как контуры глифов одного цвета.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="bd6a6-143">**Примечание.** Поддерживается начиная с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="bd6a6-144">Таблица [SVG](/typography/opentype/spec/svg)</span><span class="sxs-lookup"><span data-stu-id="bd6a6-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="bd6a6-145">Использует векторные изображения, созданные в масштабируемом векторном графическом формате.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="bd6a6-146">**Примечание.** Начиная с годовщины Windows 10, DirectWrite поддерживает подмножество полных спецификаций SVG. Не все содержимое SVG гарантированно отображается в шрифте OpenType SVG.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="bd6a6-147">Дополнительные сведения см. в разделе [Поддержка SVG](../direct2d/svg-support.md) .</span><span class="sxs-lookup"><span data-stu-id="bd6a6-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="bd6a6-148">[Кбдт](/typography/opentype/spec/cbdt) / [Кблк](/typography/opentype/spec/cblc) таблицы</span><span class="sxs-lookup"><span data-stu-id="bd6a6-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="bd6a6-149">Использует встроенные цветные растровые изображения.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="bd6a6-150">Таблица [сбикс](/typography/opentype/spec/sbix)</span><span class="sxs-lookup"><span data-stu-id="bd6a6-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="bd6a6-151">Использует встроенные цветные растровые изображения.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="bd6a6-152">Использование цветовых шрифтов</span><span class="sxs-lookup"><span data-stu-id="bd6a6-152">Using color fonts</span></span>

<span data-ttu-id="bd6a6-153">С точки зрения пользователя цветовые шрифты являются просто шрифтами.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="bd6a6-154">Например, они обычно устанавливаются и удаляются из системы так же, как монохромные шрифты, и подготавливаются к просмотру как обычный, выбираемый текст.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="bd6a6-155">С точки зрения разработчика, цветовые шрифты обычно используются так же, как монохромные шрифты.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="bd6a6-156">В платформах XAML и Microsoft ребра можно использовать цветовые шрифты так же, как обычные шрифты, и по умолчанию текст будет отображаться в цвете.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="bd6a6-157">Однако если приложение напрямую вызывает API Direct2D (или Win2D API) для отрисовки текста, оно должно явно запрашивать визуализацию цветового шрифта.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="bd6a6-158">Использование цветовых шрифтов в приложении XAML</span><span class="sxs-lookup"><span data-stu-id="bd6a6-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="bd6a6-159">Текстовые элементы платформы XAML (такие как [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [Ричедитбокс](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)и [фонтикон](/uwp/api/windows.ui.xaml.controls.fonticon)) поддерживают цветовые шрифты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="bd6a6-160">Просто создайте стиль текста с помощью цветового шрифта, и все глифы цвета будут подготавливаться к просмотру цветом.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="bd6a6-161">В следующем примере кода показан один из способов стиля элемента управления TextBlock с помощью цветового шрифта, упакованного в приложение.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="bd6a6-162">Тот же метод применяется к обычным шрифтам.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="bd6a6-163">Если вы никогда не хотите, чтобы элемент текста XAML отображал многоцветный текст, установите для его свойства [исколорфонтенабледпроперти](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) значение false.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="bd6a6-164">Использование цветовых шрифтов в Microsoft ребро</span><span class="sxs-lookup"><span data-stu-id="bd6a6-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="bd6a6-165">Цветовые шрифты отображаются по умолчанию на веб-сайтах и веб-приложениях, работающих в Microsoft погранично, включая элемент управления XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) .</span><span class="sxs-lookup"><span data-stu-id="bd6a6-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="bd6a6-166">Просто используйте HTML и CSS для стиля текста с помощью цветового шрифта, а цветовые глифы будут подготавливаться к просмотру цветом.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="bd6a6-167">Использование цветовых шрифтов с DirectWrite и Direct2D</span><span class="sxs-lookup"><span data-stu-id="bd6a6-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="bd6a6-168">Приложение может использовать методы рисования текста более высокого уровня Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) и [**дравтекстлайаут**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) или использовать методы более низкого уровня для прорисовки запуска глифов напрямую.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="bd6a6-169">В любом случае приложение требует изменения кода, чтобы правильно обрабатывались глифы цвета.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="bd6a6-170">Если приложение использует API-интерфейсы Direct2D **DrawText** и **дравтекстлайаут** , обратите внимание, что по умолчанию не отображаются глифы цвета.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="bd6a6-171">Это позволяет избежать непредвиденных изменений в работе приложений для отрисовки текста, разработанных до цветной поддержки цветовых шрифтов.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="bd6a6-172">Чтобы принять участие в визуализации цветовых глифов, передайте параметр [**D2D1 \_ Draw \_ Text (включить параметры \_ \_ \_ цветового \_ шрифта**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) ) в метод Drawing.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="bd6a6-173">В следующем примере кода показано, как вызвать метод Direct2D s DrawText для отображения строки в цветном шрифте:</span><span class="sxs-lookup"><span data-stu-id="bd6a6-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


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



<span data-ttu-id="bd6a6-174">Если приложение использует интерфейсы API более низкого уровня для обработки глифов напрямую, оно будет продолжать работать при наличии цветовых шрифтов, но не сможет рисовать цветовые глифы без дополнительной логики.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="bd6a6-175">Чтобы правильно обрабатывались цветовые глифы, приложение должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bd6a6-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="bd6a6-176">Передайте сведения о запуске глифа в [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), а также параметр [**\_ \_ \_ форматов изображения глифа дврите**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) , указывающий типы цветовых глифов, которые приложение подготовлено к обработке.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="bd6a6-177">Если имеются любые цветовые глифы (на основе шрифта и запрошенных **\_ \_ \_ форматов изображения глифа Дврите**), то DirectWrite будет разделять основной глиф, выполняемый в отдельном цветном глифе, к которому можно получить доступ с помощью возвращенного объекта [**идвритеколорглифруненумератор**](idwritecolorglyphrunenumerator.md) на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="bd6a6-178">Проверьте значение HRESULT, возвращаемое функцией [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) , чтобы определить, были ли обнаружены какие — глифы цвета.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="bd6a6-179">**Значение HRESULT** для **дврите \_ E \_** указывает, что соответствующий цвет глифа цвета не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="bd6a6-180">Если [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) не запустил цветовой глиф (путем возвращения **дврите \_ E \_ Color**), то весь фрагмент глифа рассматривается как монохромный, и приложение должно нарисовать его по желанию (например, с помощью [**ID2D1DeviceContext::D равглифрун**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span><span class="sxs-lookup"><span data-stu-id="bd6a6-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="bd6a6-181">Если [**транслатеколорглифрун**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) сообщает о наличии цветового глифа, приложение должно игнорировать выполнение основного глифа, а вместо этого использовать число запусков глифов цвета, возвращенных транслатеколорглифрун.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="bd6a6-182">Для этого выполните итерацию возвращенного объекта [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) , извлекая каждый цветовой глиф и нарисовав его в соответствии с форматом изображения глифа (например, можно использовать [**дравколорбитмапглифрун**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) и [**дравсвгглифрун**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) для рисования цветных глифов и глифов SVG соответственно).</span><span class="sxs-lookup"><span data-stu-id="bd6a6-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="bd6a6-183">В следующем примере кода показана общая структура этой процедуры:</span><span class="sxs-lookup"><span data-stu-id="bd6a6-183">The following code example shows the general structure of this procedure:</span></span>


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



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="bd6a6-184">Использование цветовых шрифтов с Win2D</span><span class="sxs-lookup"><span data-stu-id="bd6a6-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="bd6a6-185">Как и в API-интерфейсах Direct2D, Win2D s, по умолчанию не отображаются цветовые глифы.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="bd6a6-186">Чтобы принять участие в визуализации цветовых глифов, установите флаг параметров [енаблеколорфонт](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) в объекте текстового формата, который приложение передает в метод рисования текста.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="bd6a6-187">В следующем примере кода показано, как визуализировать строку в цветовой шрифт с помощью Win2D:</span><span class="sxs-lookup"><span data-stu-id="bd6a6-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="bd6a6-188">См. также</span><span class="sxs-lookup"><span data-stu-id="bd6a6-188">Related topics</span></span>

[<span data-ttu-id="bd6a6-189">Образец цветового глифа DirectWrite</span><span class="sxs-lookup"><span data-stu-id="bd6a6-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="bd6a6-190">**Интерфейс IDWriteFontFace4**</span><span class="sxs-lookup"><span data-stu-id="bd6a6-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="bd6a6-191">**Метод IDWriteFactory4:: Транслатеколорглифрун**</span><span class="sxs-lookup"><span data-stu-id="bd6a6-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="bd6a6-192">**ID2D1DeviceContext4: метод:D Равтекст**</span><span class="sxs-lookup"><span data-stu-id="bd6a6-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

