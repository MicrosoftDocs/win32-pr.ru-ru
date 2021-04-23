---
description: В этом разделе описывается запись текста в объектную модель XPS.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Запись текста в объектную модель XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cca953d5281620cf7b7d9b7b07c133bee0d4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265346"
---
# <a name="write-text-to-an-xps-om"></a><span data-ttu-id="3f43e-103">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-103">Write Text to an XPS OM</span></span>

<span data-ttu-id="3f43e-104">В этом разделе описывается запись текста в объектную модель XPS.</span><span class="sxs-lookup"><span data-stu-id="3f43e-104">This topic describes how to write text to an XPS OM.</span></span>

<span data-ttu-id="3f43e-105">Текст помещается в объектную модель XPS путем создания и форматирования интерфейса [**икспсомглифс**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) и последующего добавления интерфейса **икспсомглифс** в список визуальных объектов страницы или холста.</span><span class="sxs-lookup"><span data-stu-id="3f43e-105">Text is placed in an XPS OM by creating and formatting an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface and then adding the **IXpsOMGlyphs** interface to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="3f43e-106">Каждый интерфейс **икспсомглифс** представляет выполнение глифа, которое представляет собой непрерывный запуск символов с общим форматом.</span><span class="sxs-lookup"><span data-stu-id="3f43e-106">Each **IXpsOMGlyphs** interface represents a glyph run, which is a continuous run of characters that share a common format.</span></span> <span data-ttu-id="3f43e-107">При изменении элемента символьного формата (например, типа шрифта или размера) или разрыва строки необходимо создать новый интерфейс **икспсомглифс** и добавить его в список визуальных объектов.</span><span class="sxs-lookup"><span data-stu-id="3f43e-107">When a character format element (such as font type or size) changes or when a line breaks, a new **IXpsOMGlyphs** interface must be created and added to the list of visual objects.</span></span>

<span data-ttu-id="3f43e-108">Некоторые свойства запуска глифа можно задать с помощью методов интерфейса [**икспсомглифс**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) .</span><span class="sxs-lookup"><span data-stu-id="3f43e-108">Some of the properties of a glyph run can be set by using the methods of the [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface.</span></span> <span data-ttu-id="3f43e-109">Некоторые свойства, однако, взаимодействуют с другими и должны устанавливаться с помощью интерфейса [**икспсомглифседитор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) .</span><span class="sxs-lookup"><span data-stu-id="3f43e-109">Some properties, however, interact with others and must be set by using an [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) interface.</span></span>

<span data-ttu-id="3f43e-110">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3f43e-110">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="3f43e-111">Пример кода</span><span class="sxs-lookup"><span data-stu-id="3f43e-111">Code Example</span></span>

### <a name="create-a-glyph-run-from-a-string"></a><span data-ttu-id="3f43e-112">Создание глифа выполнение из строки</span><span class="sxs-lookup"><span data-stu-id="3f43e-112">Create a glyph run from a string</span></span>

<span data-ttu-id="3f43e-113">Выполнение глифа обычно создается в несколько шагов, включая загрузку ресурсов шрифта, используемых глифами, задание кисти заливки, указание размера шрифта и начального расположения, а также задание строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3f43e-113">A glyph run is commonly created in several steps that include loading the font resources that are used by the glyph run, setting a fill brush, specifying the font size and starting location, and setting the Unicode string.</span></span>

<span data-ttu-id="3f43e-114">В следующем разделе примера кода содержится подпрограмма, принимающая некоторые переменные, включая размер, цвет и расположение шрифта, а также символы, которые необходимо записать.</span><span class="sxs-lookup"><span data-stu-id="3f43e-114">The following section of the code example contains a routine that accepts some variables, including the font size, color and location, and the characters to be written.</span></span> <span data-ttu-id="3f43e-115">Затем код создает выполнение глифа и добавляет его на страницу.</span><span class="sxs-lookup"><span data-stu-id="3f43e-115">The code then creates a glyph run and then adds it to a page.</span></span> <span data-ttu-id="3f43e-116">В примере кода предполагается, что была выполнена инициализация, описанная в разделе [Инициализация OM-модели XPS](xps-object-model-initialization.md) и что у документа есть хотя бы одна страница.</span><span class="sxs-lookup"><span data-stu-id="3f43e-116">The code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has occurred and that the document has at least one page.</span></span> <span data-ttu-id="3f43e-117">Дополнительные сведения о создании пустой модели XPS см. в статье [Создание пустой](create-a-blank-xps-om.md)ОБЪЕКТной модели XPS.</span><span class="sxs-lookup"><span data-stu-id="3f43e-117">For more information about creating a blank XPS OM, refer to [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a><span data-ttu-id="3f43e-118">Загрузка и создание ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f43e-118">Load and create resources</span></span>

<span data-ttu-id="3f43e-119">Для создания интерфейса [**икспсомглифс**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) требуется ресурс шрифта.</span><span class="sxs-lookup"><span data-stu-id="3f43e-119">Creation of an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface requires a font resource.</span></span> <span data-ttu-id="3f43e-120">Во многих случаях блок текста использует один и тот же шрифт и цвет.</span><span class="sxs-lookup"><span data-stu-id="3f43e-120">In many cases, a block of text uses the same font and color.</span></span> <span data-ttu-id="3f43e-121">Поэтому в этом разделе примера кода создаются интерфейсы ресурсов шрифтов, которые будут использоваться в вызовах, которые размещают текст на странице.</span><span class="sxs-lookup"><span data-stu-id="3f43e-121">Hence, this section of the code example will create the font resource interfaces that will be used in the calls that place the text on the page.</span></span>


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a><span data-ttu-id="3f43e-122">Рисование текста на странице</span><span class="sxs-lookup"><span data-stu-id="3f43e-122">Draw text in a page</span></span>

<span data-ttu-id="3f43e-123">В последнем разделе примера кода выполняется создание глифа для каждого выполнения аналогичного форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="3f43e-123">The final section of the code example creates the glyph runs for each run of similarly formatted text.</span></span> <span data-ttu-id="3f43e-124">Чтобы выполнить код в этом последнем разделе, необходимо создать экземпляр и инициализировать интерфейс **кспсфактори** , а также ресурс шрифта и цветовую кисть текста.</span><span class="sxs-lookup"><span data-stu-id="3f43e-124">To execute the code in this final section, the **xpsFactory** interface as well as the font resource and a text color brush are necessary and must have been instantiated and initialized.</span></span> <span data-ttu-id="3f43e-125">В этом примере функция, описанная в первом разделе, используется для создания глифа и добавления их на страницу.</span><span class="sxs-lookup"><span data-stu-id="3f43e-125">In this example, the function described in the first section is used to create the glyph runs and to add them to the page.</span></span>


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a><span data-ttu-id="3f43e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3f43e-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3f43e-127">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="3f43e-127">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="3f43e-128">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-128">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3f43e-129">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3f43e-130">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3f43e-131">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-131">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="3f43e-132">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-132">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="3f43e-133">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="3f43e-133">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="3f43e-134">**иопкпартури**</span><span class="sxs-lookup"><span data-stu-id="3f43e-134">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="3f43e-135">**икспсомфонтресаурце**</span><span class="sxs-lookup"><span data-stu-id="3f43e-135">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="3f43e-136">**икспсомглифс**</span><span class="sxs-lookup"><span data-stu-id="3f43e-136">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[<span data-ttu-id="3f43e-137">**икспсомглифседитор**</span><span class="sxs-lookup"><span data-stu-id="3f43e-137">**IXpsOMGlyphsEditor**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[<span data-ttu-id="3f43e-138">**икспсомобжектфактори**</span><span class="sxs-lookup"><span data-stu-id="3f43e-138">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="3f43e-139">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="3f43e-139">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="3f43e-140">**икспсомсолидколорбруш**</span><span class="sxs-lookup"><span data-stu-id="3f43e-140">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="3f43e-141">**икспсомвисуал**</span><span class="sxs-lookup"><span data-stu-id="3f43e-141">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="3f43e-142">**икспсомвисуалколлектион**</span><span class="sxs-lookup"><span data-stu-id="3f43e-142">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="3f43e-143">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="3f43e-143">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="3f43e-144">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-144">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="3f43e-145">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-145">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="3f43e-146">XPS</span><span class="sxs-lookup"><span data-stu-id="3f43e-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
