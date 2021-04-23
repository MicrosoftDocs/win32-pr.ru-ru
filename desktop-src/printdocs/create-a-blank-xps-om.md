---
description: В этом разделе описывается создание пустой модели XPS.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Создание пустой объектной модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702215"
---
# <a name="create-a-blank-xps-om"></a><span data-ttu-id="3d4f0-103">Создание пустой объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-103">Create a Blank XPS OM</span></span>

<span data-ttu-id="3d4f0-104">В этом разделе описывается создание пустой модели XPS.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-104">This topic describes how to create a blank XPS OM.</span></span> <span data-ttu-id="3d4f0-105">В нем представлены примеры кода, иллюстрирующие использование OM XPS для создания структуры документа XPS-документа с одной пустой страницей.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-105">It presents the code examples that illustrate how to use an XPS OM to build the document structure of an XPS document that has one blank page.</span></span>

<span data-ttu-id="3d4f0-106">Для сохранения в виде документа XPS необходимо по крайней мере следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="3d4f0-106">To be saved as an XPS document, the XPS OM requires at least the following components:</span></span>

-   <span data-ttu-id="3d4f0-107">[**Икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , описывающий пакет документа XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-107">An [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) that describes the XPS document package</span></span>
-   <span data-ttu-id="3d4f0-108">Объект [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , содержащий структуру содержимого пакета.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-108">An [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) that contains the framework of the package contents</span></span>
-   <span data-ttu-id="3d4f0-109">Объект [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) , содержащий платформу документа в пакете</span><span class="sxs-lookup"><span data-stu-id="3d4f0-109">An [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) that contains the framework of a document within the package</span></span>
-   <span data-ttu-id="3d4f0-110">Объект [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) , содержащий коллекцию страниц в документе</span><span class="sxs-lookup"><span data-stu-id="3d4f0-110">An [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) that contains the collection of pages in the document</span></span>
-   <span data-ttu-id="3d4f0-111">Объект [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , содержащий пустую страницу</span><span class="sxs-lookup"><span data-stu-id="3d4f0-111">An [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) that contains a blank page</span></span>

<span data-ttu-id="3d4f0-112">При использовании этих интерфейсов объектная модель XPS будет содержать документ с одной пустой страницей.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-112">When these interfaces are used, the XPS OM will contain a document that has one blank page.</span></span> <span data-ttu-id="3d4f0-113">Чтобы создать этот документ в объектной модели XPS, программа должна сначала создать отдельные компоненты, а затем связать их вместе.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-113">To create this document in an XPS OM, the program must first create the individual components and then link them together.</span></span>

<span data-ttu-id="3d4f0-114">Перед использованием приведенных ниже примеров кода прочитайте заявление об отказе в [распространенных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3d4f0-114">Before using the following code examples, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-examples"></a><span data-ttu-id="3d4f0-115">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="3d4f0-115">Code Examples</span></span>

<span data-ttu-id="3d4f0-116">В следующем примере кода предполагается, что инициализация, описанная в разделе [Инициализация объектной модели XPS](xps-object-model-initialization.md), прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-116">The following code example assumes that the initialization, described in [Initialize an XPS OM](xps-object-model-initialization.md), has succeeded.</span></span>


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a><span data-ttu-id="3d4f0-117">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="3d4f0-117">Best Practices</span></span>

<span data-ttu-id="3d4f0-118">После того как вы использовали интерфейс [**иопкпартури**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) для создания компонента (например, после вызова метода **CreateDocument** в примере кода), отпустите указатель на этот интерфейс, если это не требуется для другого вызова.</span><span class="sxs-lookup"><span data-stu-id="3d4f0-118">After you have used an [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface to create a component (such as after calling the **CreateDocument** method in the code example), release the pointer to that interface—unless you need it for another call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d4f0-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3d4f0-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3d4f0-120">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="3d4f0-121">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-121">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3d4f0-122">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-122">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3d4f0-123">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-123">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3d4f0-124">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-124">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="3d4f0-125">**Используется на этой странице**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-125">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="3d4f0-126">**иопкпартури**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-126">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="3d4f0-127">**икспсомобжектфактори**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-127">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="3d4f0-128">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-128">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="3d4f0-129">**икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-129">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="3d4f0-130">**икспсомдокументколлектион**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-130">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="3d4f0-131">**икспсомдокумент**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-131">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="3d4f0-132">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-132">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="3d4f0-133">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-133">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="3d4f0-134">**икспсомпажереференцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-134">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="3d4f0-135">**\_Размер XPS**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-135">**XPS\_SIZE**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

<span data-ttu-id="3d4f0-136">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="3d4f0-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="3d4f0-137">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-137">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="3d4f0-138">API для упаковки</span><span class="sxs-lookup"><span data-stu-id="3d4f0-138">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="3d4f0-139">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-139">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="3d4f0-140">XPS</span><span class="sxs-lookup"><span data-stu-id="3d4f0-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
