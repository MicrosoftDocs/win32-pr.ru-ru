---
title: Форматирование и макет текста
description: DirectWrite предоставляет два интерфейса для форматирования текста Идвритетекстформат и Идвритетекстлайаут.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, форматирование текста
- DirectWrite, макет
- DirectWrite, интерфейс Идвритетекстформат
- DirectWrite, интерфейс Идвритетекстлайаут
- Интерфейс Идвритетекстформат
- Интерфейс Идвритетекстлайаут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380758"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="a3fac-109">Форматирование и макет текста</span><span class="sxs-lookup"><span data-stu-id="a3fac-109">Text Formatting and Layout</span></span>

<span data-ttu-id="a3fac-110">[DirectWrite](direct-write-portal.md) предоставляет два интерфейса для форматирования текста: [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) и [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="a3fac-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="a3fac-111">**Идвритетекстформат** описывает только формат текста и используется в тех случаях, когда вся строка имеет одинаковый размер, стиль, вес и т. д.</span><span class="sxs-lookup"><span data-stu-id="a3fac-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="a3fac-112">С другой стороны, **идвритетекстлайаут** инкапсулирует текстовую строку и форматирование для указанных диапазонов строки.</span><span class="sxs-lookup"><span data-stu-id="a3fac-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="a3fac-113">В этом документе описывается каждый интерфейс и их использование.</span><span class="sxs-lookup"><span data-stu-id="a3fac-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="a3fac-114">Дополнительные сведения о создании и методах этих интерфейсов см. на страницах справочника по [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) и [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="a3fac-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="a3fac-115">Этот документ содержит следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="a3fac-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="a3fac-116">идвритетекстформат</span><span class="sxs-lookup"><span data-stu-id="a3fac-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="a3fac-117">Изменение Идвритетекстформат</span><span class="sxs-lookup"><span data-stu-id="a3fac-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="a3fac-118">идвритетекстлайаут</span><span class="sxs-lookup"><span data-stu-id="a3fac-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="a3fac-119">Форматирование диапазона текста</span><span class="sxs-lookup"><span data-stu-id="a3fac-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="a3fac-120">Параметры подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="a3fac-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="a3fac-121">идвритетекстформат</span><span class="sxs-lookup"><span data-stu-id="a3fac-121">IDWriteTextFormat</span></span>

<span data-ttu-id="a3fac-122">Объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) используется для:</span><span class="sxs-lookup"><span data-stu-id="a3fac-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="a3fac-123">Опишите формат всей строки при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="a3fac-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="a3fac-124">Чтобы отобразить строку с несколькими форматами, используйте объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="a3fac-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="a3fac-125">При создании объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) укажите формат текста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3fac-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="a3fac-126">Чтобы создать объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , используйте метод [**Идвритефактори:: креатетекстформат**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) и укажите семейство шрифтов, коллекцию шрифтов, плотность шрифта, размер шрифта (в DIP), имя локали.</span><span class="sxs-lookup"><span data-stu-id="a3fac-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="a3fac-127">Изменение Идвритетекстформат</span><span class="sxs-lookup"><span data-stu-id="a3fac-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="a3fac-128">После создания интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) некоторые значения не могут быть изменены: семейство шрифтов, коллекция, вес и размер, а также имя локали.</span><span class="sxs-lookup"><span data-stu-id="a3fac-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="a3fac-129">Чтобы изменить эти значения, необходимо создать новый объект **идвритетекстформат** .</span><span class="sxs-lookup"><span data-stu-id="a3fac-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="a3fac-130">[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) позволяет изменить приведенные выше свойства, не создавая ничего.</span><span class="sxs-lookup"><span data-stu-id="a3fac-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anything.</span></span> <span data-ttu-id="a3fac-131">[**Идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) позволяет вносить изменения формата, применяемые ко всему тексту, например выравнивание текста.</span><span class="sxs-lookup"><span data-stu-id="a3fac-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="a3fac-132">Если вы хотите применить форматирование к конкретным диапазонам символов, это следует сделать с помощью **идвритетекстлайаут**.</span><span class="sxs-lookup"><span data-stu-id="a3fac-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="a3fac-133">[**Идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) предоставляет методы для задания выравнивания текста, направления потока, инкрементной табуляции, интервала между строками, выравнивания абзаца, обрезки и переноса слов.</span><span class="sxs-lookup"><span data-stu-id="a3fac-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="a3fac-134">Эти свойства можно изменить в любое время после создания объекта **идвритетекстформат** .</span><span class="sxs-lookup"><span data-stu-id="a3fac-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="a3fac-135">идвритетекстлайаут</span><span class="sxs-lookup"><span data-stu-id="a3fac-135">IDWriteTextLayout</span></span>

<span data-ttu-id="a3fac-136">Интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , в отличие от [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), представляет как блок текста, так и связанное форматирование.</span><span class="sxs-lookup"><span data-stu-id="a3fac-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="a3fac-137">**Идвритетекстформат** представляет сведения о начальном форматировании.</span><span class="sxs-lookup"><span data-stu-id="a3fac-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="a3fac-138">В следующем примере показано, как создать объект **идвритетекстлайаут** с помощью [**Идвритефактори:: креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span><span class="sxs-lookup"><span data-stu-id="a3fac-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



<span data-ttu-id="a3fac-139">Текст в объекте [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) не может быть изменен после создания объекта.</span><span class="sxs-lookup"><span data-stu-id="a3fac-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="a3fac-140">Чтобы изменить текст, необходимо удалить существующий объект и создать новый объект **идвритетекстлайаут** .</span><span class="sxs-lookup"><span data-stu-id="a3fac-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="a3fac-141">Для форматирования указанных диапазонов текста можно использовать [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="a3fac-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="a3fac-142">**Идвритетекстлайаут** также предоставляет методы для изменения стиля и веса шрифта и добавления функций шрифтов OpenType и проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="a3fac-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="a3fac-143">Дополнительные сведения и полный список методов см. на странице справочника по [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="a3fac-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="a3fac-144">Форматирование диапазона текста</span><span class="sxs-lookup"><span data-stu-id="a3fac-144">Formatting a range of text</span></span>

<span data-ttu-id="a3fac-145">[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) предоставляет несколько методов для форматирования диапазонов текста.</span><span class="sxs-lookup"><span data-stu-id="a3fac-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="a3fac-146">Каждый из этих методов принимает в качестве параметра структуру [**\_ \_ диапазона текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) , чтобы указать начальную текстовую точку в строке и длину диапазона для форматирования.</span><span class="sxs-lookup"><span data-stu-id="a3fac-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="a3fac-147">В следующем примере показано, как задать полужирным шрифтом начертание шрифта для диапазона текста.</span><span class="sxs-lookup"><span data-stu-id="a3fac-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="a3fac-148">Параметры подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="a3fac-148">Rendering Options</span></span>

<span data-ttu-id="a3fac-149">Текст с форматированием, описанным только в объекте [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , может быть визуализирован с помощью [Direct2D](../direct2d/direct2d-portal.md), однако существует несколько дополнительных параметров для отрисовки объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="a3fac-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="a3fac-150">Строку, описываемую объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , можно визуализировать с помощью методов, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="a3fac-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="a3fac-151">[Прорисовка с помощью Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="a3fac-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="a3fac-152">[Отрисовка с помощью пользовательского модуля подготовки текста](how-to-implement-a-custom-text-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="a3fac-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="a3fac-153">[Подготовка к просмотру на поверхности GDI](render-to-a-gdi-surface.md).</span><span class="sxs-lookup"><span data-stu-id="a3fac-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 
