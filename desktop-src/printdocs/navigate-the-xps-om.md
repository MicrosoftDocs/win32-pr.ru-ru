---
description: В этом разделе описывается, как перемещаться по модели XPS и обращаться к различным частям документа в памяти.
ms.assetid: 90b726aa-29da-4cfb-9c69-f471c2acb678
title: Навигация по OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ec33543867f66dd4da65ef95aab0cdfd8cfe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684038"
---
# <a name="navigate-the-xps-om"></a><span data-ttu-id="bd65d-103">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-103">Navigate the XPS OM</span></span>

<span data-ttu-id="bd65d-104">В этом разделе описывается, как перемещаться по модели XPS и обращаться к различным частям документа в памяти.</span><span class="sxs-lookup"><span data-stu-id="bd65d-104">This topic describes how to navigate an XPS OM and to access different parts of the in-memory document.</span></span>

<span data-ttu-id="bd65d-105">Организация API документов XPS дублирует организацию документа XPS.</span><span class="sxs-lookup"><span data-stu-id="bd65d-105">The organization of the XPS Document API mirrors the organization of an XPS document.</span></span> <span data-ttu-id="bd65d-106">В следующей таблице показано, как интерфейсы API документа XPS связаны с компонентами документа XPS.</span><span class="sxs-lookup"><span data-stu-id="bd65d-106">The following table illustrates how the interfaces of the XPS Document API relate to the components of an XPS document.</span></span>



| <span data-ttu-id="bd65d-107">Компонент документа XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-107">XPS document component</span></span>                                         | <span data-ttu-id="bd65d-108">Интерфейс API документов XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-108">XPS Document API interface</span></span>                                          | <span data-ttu-id="bd65d-109">Метод для вызова следующего уровня в иерархии</span><span class="sxs-lookup"><span data-stu-id="bd65d-109">Method to call for the next level down in the hierarchy</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd65d-110">Файл документа XPS (содержит пакет OPC)</span><span class="sxs-lookup"><span data-stu-id="bd65d-110">XPS document file (contains OPC package)</span></span><br/>            | [<span data-ttu-id="bd65d-111">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="bd65d-111">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>                   | [<span data-ttu-id="bd65d-112">**жетдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-112">**GetDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence)<br/>                                                                   |
| <span data-ttu-id="bd65d-113">Часть FixedDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="bd65d-113">FixedDocumentSequence part</span></span><br/>                          | [<span data-ttu-id="bd65d-114">**икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-114">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [<span data-ttu-id="bd65d-115">**GetDocuments**</span><span class="sxs-lookup"><span data-stu-id="bd65d-115">**GetDocuments**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getdocuments)<br/>                                                                        |
| <span data-ttu-id="bd65d-116">Часть FixedDocument</span><span class="sxs-lookup"><span data-stu-id="bd65d-116">FixedDocument part</span></span><br/>                                  | [<span data-ttu-id="bd65d-117">**икспсомдокумент**</span><span class="sxs-lookup"><span data-stu-id="bd65d-117">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [<span data-ttu-id="bd65d-118">**жетпажереференцес**</span><span class="sxs-lookup"><span data-stu-id="bd65d-118">**GetPageReferences**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getpagereferences)<br/>                                                                      |
| <span data-ttu-id="bd65d-119">Элемент **PageContent** в разметке FixedDocument</span><span class="sxs-lookup"><span data-stu-id="bd65d-119">**PageContent** element in the FixedDocument markup</span></span><br/> | [<span data-ttu-id="bd65d-120">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-120">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [<span data-ttu-id="bd65d-121">**GetPage.**</span><span class="sxs-lookup"><span data-stu-id="bd65d-121">**GetPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)<br/> [<span data-ttu-id="bd65d-122">**коллектпартресаурцес**</span><span class="sxs-lookup"><span data-stu-id="bd65d-122">**CollectPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources)<br/> |
| <span data-ttu-id="bd65d-123">Элемент FixedPage</span><span class="sxs-lookup"><span data-stu-id="bd65d-123">FixedPage part</span></span><br/>                                      | [<span data-ttu-id="bd65d-124">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="bd65d-124">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                         | [<span data-ttu-id="bd65d-125">**Визуализация**</span><span class="sxs-lookup"><span data-stu-id="bd65d-125">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals)<br/>                                                                                        |
| <span data-ttu-id="bd65d-126">**Canvas** , элемент в разметке FixedPage</span><span class="sxs-lookup"><span data-stu-id="bd65d-126">**Canvas** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="bd65d-127">**икспсомканвас**</span><span class="sxs-lookup"><span data-stu-id="bd65d-127">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/>                     | [<span data-ttu-id="bd65d-128">**Визуализация**</span><span class="sxs-lookup"><span data-stu-id="bd65d-128">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals)<br/>                                                                                      |
| <span data-ttu-id="bd65d-129">Элемент **path** в разметке FixedPage</span><span class="sxs-lookup"><span data-stu-id="bd65d-129">**Path** element in the FixedPage markup</span></span><br/>            | [<span data-ttu-id="bd65d-130">**икспсомпас**</span><span class="sxs-lookup"><span data-stu-id="bd65d-130">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                         | <span data-ttu-id="bd65d-131">Конец иерархии документа.</span><span class="sxs-lookup"><span data-stu-id="bd65d-131">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="bd65d-132">Элемент **Glyphs** в разметке FixedPage</span><span class="sxs-lookup"><span data-stu-id="bd65d-132">**Glyphs** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="bd65d-133">**икспсомглифс**</span><span class="sxs-lookup"><span data-stu-id="bd65d-133">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/>                     | <span data-ttu-id="bd65d-134">Конец иерархии документа.</span><span class="sxs-lookup"><span data-stu-id="bd65d-134">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="bd65d-135">Часть шрифта</span><span class="sxs-lookup"><span data-stu-id="bd65d-135">Font part</span></span><br/>                                           | [<span data-ttu-id="bd65d-136">**икспсомфонтресаурце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-136">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)<br/>         | <span data-ttu-id="bd65d-137">Конец иерархии документа.</span><span class="sxs-lookup"><span data-stu-id="bd65d-137">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="bd65d-138">Часть изображения</span><span class="sxs-lookup"><span data-stu-id="bd65d-138">Image part</span></span><br/>                                          | [<span data-ttu-id="bd65d-139">**икспсомимажересаурце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-139">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)<br/>       | <span data-ttu-id="bd65d-140">Конец иерархии документа.</span><span class="sxs-lookup"><span data-stu-id="bd65d-140">End of document hierarchy.</span></span><br/>                                                                                                         |



 

<span data-ttu-id="bd65d-141">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="bd65d-141">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="bd65d-142">Пример кода</span><span class="sxs-lookup"><span data-stu-id="bd65d-142">Code Example</span></span>

<span data-ttu-id="bd65d-143">В следующем примере кода предполагается существование инициализированной OM-модели XPS, а *пакет* указывает на интерфейс [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , который представляет эту модель XPS.</span><span class="sxs-lookup"><span data-stu-id="bd65d-143">The following code example assumes the existence of an initialized XPS OM, and *package* points to an [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface that represents that XPS OM.</span></span> <span data-ttu-id="bd65d-144">Сведения о создании объектной модели XPS см. [в статье чтение XPS-документа в объектную модель XPS](read-an-xps-document-into-an-xps-om.md) или [Создание пустой модели XPS](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="bd65d-144">For information about creating an XPS OM, see [Read an XPS Document into an XPS OM](read-an-xps-document-into-an-xps-om.md) or [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
    HRESULT                        hr = S_OK;

    IXpsOMDocumentSequence         *docSeq = NULL;
    IXpsOMDocumentCollection       *docs = NULL;
    IXpsOMDocument                 *doc = NULL;
    IXpsOMPageReferenceCollection  *pages = NULL;
    IXpsOMPageReference            *pageRef = NULL;
    IXpsOMPage                     *page = NULL;
    IXpsOMCanvas                   *canvas = NULL;
    IXpsOMPath                     *path = NULL;
    IXpsOMPartResources            *pageParts = NULL;
    IXpsOMGlyphs                   *glyphs = NULL;
    IXpsOMFontResourceCollection   *fonts = NULL; 
    IXpsOMFontResource             *font = NULL;
    IXpsOMImageResourceCollection  *images = NULL;
    IXpsOMImageResource            *image = NULL;
    IXpsOMVisualCollection         *visuals = NULL;
    IXpsOMVisual                   *visual = NULL;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    UINT32  numVisuals = 0;
    UINT32  thisVisual = 0;

    UINT32  numFonts = 0;
    UINT32  thisFont = 0;

    UINT32  numImages = 0;
    UINT32  thisImage = 0;

    XPS_OBJECT_TYPE  visualType;
 
    // package points to the IXpsOMPackage interface to walk.

    // Get the fixed document sequence of the package.
    hr = package->GetDocumentSequence(&docSeq);

    // Get the fixed documents in the fixed document sequence.
    hr = docSeq->GetDocuments(&docs);

    // Walk the collection of documents.
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // Get the doc contents.
        hr = doc->GetPageReferences(&pages);
        
        // Walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // Get this page reference.
            hr = pages->GetAt(thisPageRef, &pageRef);

            // Get the page content of this page reference.
            {
                hr = pageRef->GetPage (&page);

                // Get the visual tree of this page.
                hr = page->GetVisuals (&visuals);
                
                // Walk the visuals.
                hr = visuals->GetCount (&numVisuals);
                thisVisual = 0;
                while (thisVisual < numVisuals) {
                    hr = visuals->GetAt (thisVisual, &visual);
                    // Get visual type.
                    hr = visual->GetType( &visualType );
                    
                    // Do other stuff with the visual.

                    // Release the visual.
                    if (NULL != visual) {visual->Release(); visual = NULL;}
                    thisVisual++; // Get next visual in collection.
                }
                if (NULL != visuals) {visuals->Release(); visuals = NULL;}
                if (NULL != page) {page->Release(); page = NULL;}
            }
            // Get the part resources used by this page.
            hr = pageRef->CollectPartResources (&pageParts);

            // Get the font resources.
            {
                hr = pageParts->GetFontResources (&fonts);
                
                // Walk the fonts.
                hr = fonts->GetCount (&numFonts);
                thisFont = 0;
                while (thisFont < numFonts) {
                    hr = fonts->GetAt(thisFont, &font);
                    if (NULL != font) {font->Release(); font = NULL;}

                    thisFont++; // Get the next font in collection.
                }
                if (NULL != fonts) {fonts->Release(); fonts = NULL;}
            }

            // Get the image resources.
            {
                hr = pageParts->GetImageResources (&images);

                // walk the images
                hr = images->GetCount (&numImages);
                thisImage = 0;
                while (thisImage < numImages) {
                    hr = images->GetAt(thisImage, &image);
                    thisImage++;
                    if (NULL != image) {image->Release(); image = NULL;}
                }
                if (NULL != images) {images->Release(); images = NULL;}
            }
            if (NULL != pageRef) {pageRef->Release(); pageRef = NULL;}
            thisPageRef++; // Get next page in doc.
        }
        if (NULL != pages) {pages->Release(); pages = NULL;}
        if (NULL != doc) {doc->Release(); doc = NULL;}
        thisDoc++; // Get next doc in collection.
    }

    // Release interface pointers.
    if (NULL != docs) docs->Release();
    if (NULL != docSeq) docSeq->Release();

```



## <a name="related-topics"></a><span data-ttu-id="bd65d-145">См. также</span><span class="sxs-lookup"><span data-stu-id="bd65d-145">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bd65d-146">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="bd65d-146">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="bd65d-147">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-147">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="bd65d-148">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-148">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="bd65d-149">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-149">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="bd65d-150">**Используется на этой странице**</span><span class="sxs-lookup"><span data-stu-id="bd65d-150">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="bd65d-151">**икспсомдокумент**</span><span class="sxs-lookup"><span data-stu-id="bd65d-151">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="bd65d-152">**икспсомдокументколлектион**</span><span class="sxs-lookup"><span data-stu-id="bd65d-152">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="bd65d-153">**икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-153">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="bd65d-154">**икспсомфонтресаурце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-154">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="bd65d-155">**икспсомфонтресаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="bd65d-155">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)
</dt> <dt>

[<span data-ttu-id="bd65d-156">**икспсомимажересаурце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-156">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[<span data-ttu-id="bd65d-157">**икспсомимажересаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="bd65d-157">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)
</dt> <dt>

[<span data-ttu-id="bd65d-158">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="bd65d-158">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="bd65d-159">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="bd65d-159">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="bd65d-160">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="bd65d-160">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="bd65d-161">**икспсомпажереференцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="bd65d-161">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="bd65d-162">**икспсомвисуал**</span><span class="sxs-lookup"><span data-stu-id="bd65d-162">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="bd65d-163">**икспсомвисуалколлектион**</span><span class="sxs-lookup"><span data-stu-id="bd65d-163">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="bd65d-164">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="bd65d-164">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="bd65d-165">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-165">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="bd65d-166">Чтение XPS-документа в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-166">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="bd65d-167">Создание пустой объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-167">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

[<span data-ttu-id="bd65d-168">API для упаковки</span><span class="sxs-lookup"><span data-stu-id="bd65d-168">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="bd65d-169">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-169">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="bd65d-170">XPS</span><span class="sxs-lookup"><span data-stu-id="bd65d-170">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

