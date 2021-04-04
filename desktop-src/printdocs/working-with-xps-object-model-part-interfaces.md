---
description: В этом разделе описывается использование интерфейсов, обеспечивающих доступ к частям документа XPS в OM-модели XPS.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: Интерфейсы частей модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81cbf17c26e4ba6c80199ee787b1ee11b28d260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998382"
---
# <a name="xps-om-part-interfaces"></a><span data-ttu-id="d795e-103">Интерфейсы частей модели XPS</span><span class="sxs-lookup"><span data-stu-id="d795e-103">XPS OM Part Interfaces</span></span>

<span data-ttu-id="d795e-104">В этом разделе описывается использование интерфейсов, обеспечивающих доступ к частям документа XPS в OM-модели XPS.</span><span class="sxs-lookup"><span data-stu-id="d795e-104">This topic describes how to use the interfaces that provide access to XPS document parts in an XPS OM.</span></span>



| <span data-ttu-id="d795e-105">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="d795e-105">Interface name</span></span>                                                                                                    | <span data-ttu-id="d795e-106">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="d795e-106">Logical child interfaces</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d795e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d795e-107">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d795e-108">**икспсомпарт**</span><span class="sxs-lookup"><span data-stu-id="d795e-108">**IXpsOMPart**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [<span data-ttu-id="d795e-109">**икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="d795e-109">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="d795e-110">**икспсомдокумент**</span><span class="sxs-lookup"><span data-stu-id="d795e-110">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [<span data-ttu-id="d795e-111">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="d795e-111">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [<span data-ttu-id="d795e-112">**икспсомкорепропертиес**</span><span class="sxs-lookup"><span data-stu-id="d795e-112">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [<span data-ttu-id="d795e-113">**икспсомресаурце**</span><span class="sxs-lookup"><span data-stu-id="d795e-113">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | <span data-ttu-id="d795e-114">Компоненты документа, составляющие структуру документа.</span><span class="sxs-lookup"><span data-stu-id="d795e-114">Document components that make up the document structure.</span></span><br/>                                          |
| [<span data-ttu-id="d795e-115">**икспсомресаурце**</span><span class="sxs-lookup"><span data-stu-id="d795e-115">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [<span data-ttu-id="d795e-116">**икспсомпартресаурцес**</span><span class="sxs-lookup"><span data-stu-id="d795e-116">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | <span data-ttu-id="d795e-117">икспсомфонтресаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-117">IXpsOMFontResource</span></span><br/> <span data-ttu-id="d795e-118">икспсомимажересаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-118">IXpsOMImageResource</span></span><br/> <span data-ttu-id="d795e-119">икспсомколорпрофилересаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-119">IXpsOMColorProfileResource</span></span><br/> <span data-ttu-id="d795e-120">икспсомпринттиккетресаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-120">IXpsOMPrintTicketResource</span></span><br/> <span data-ttu-id="d795e-121">икспсомремотедиктионариресаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-121">IXpsOMRemoteDictionaryResource</span></span><br/> <span data-ttu-id="d795e-122">икспсомдокументструктурересаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-122">IXpsOMDocumentStructureResource</span></span><br/> <span data-ttu-id="d795e-123">икспсомсторифрагментсресаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-123">IXpsOMStoryFragmentsResource</span></span><br/> <span data-ttu-id="d795e-124">икспсомсигнатуреблоккресаурце</span><span class="sxs-lookup"><span data-stu-id="d795e-124">IXpsOMSignatureBlockResource</span></span><br/> | <span data-ttu-id="d795e-125">Компоненты документа, содержащие элементы, используемые или на которые ссылается страница или документ.</span><span class="sxs-lookup"><span data-stu-id="d795e-125">Document components that contain elements that are used in or referenced by a page or a document.</span></span><br/> |
| [<span data-ttu-id="d795e-126">**икспсомпартуриколлектион**</span><span class="sxs-lookup"><span data-stu-id="d795e-126">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | <span data-ttu-id="d795e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d795e-127">None</span></span><br/>                                                                                                                                                                                                                                                                                              | <span data-ttu-id="d795e-128">Коллекция URI частей.</span><span class="sxs-lookup"><span data-stu-id="d795e-128">A collection of part URIs.</span></span><br/>                                                                        |



 

## <a name="code-examples"></a><span data-ttu-id="d795e-129">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="d795e-129">Code Examples</span></span>

<span data-ttu-id="d795e-130">В приведенных ниже примерах кода показаны два примера использования интерфейсов частей для доступа к содержимому объектной модели XPS.</span><span class="sxs-lookup"><span data-stu-id="d795e-130">The code examples that follow show two examples of how to use the part interfaces to access XPS OM content.</span></span>

### <a name="get-the-name-of-a-document-part"></a><span data-ttu-id="d795e-131">Получение имени части документа</span><span class="sxs-lookup"><span data-stu-id="d795e-131">Get the name of a document part</span></span>

<span data-ttu-id="d795e-132">В следующем примере кода выполняется переход к части документа и получение имени части.</span><span class="sxs-lookup"><span data-stu-id="d795e-132">The following code example navigates to a document part and gets the part's name.</span></span>


```C++
    HRESULT                         hr = S_OK;
    
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;
    IXpsOMPageReferenceCollection   *pages;
    IXpsOMPageReference             *pageRef;
    IXpsOMPage                      *page;

    IOpcPartUri                     *thisDocPartUri;
    IOpcPartUri                     *thisPagePartUri;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // package points to the IXpsOMPackage interface to walk.

    // get the fixed document sequence of the package
    hr = package->GetDocumentSequence(&docSeq);

    // get the fixed documents in the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // get the part name (URI) of this document
        hr = doc->GetPartName ( &thisDocPartUri );

        // get the doc contents
        hr = doc->GetPageReferences(&pages);
        
        // walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // get this page reference
            hr = pages->GetAt(thisPageRef, &pageRef );

            // get the part name (URI) of this page
            hr = pageRef->GetPage (&page);
            hr = page->GetPartName ( &thisPagePartUri );

            // do something with the part name
 
            thisPagePartUri->Release();
            page->Release();
            pageRef->Release();

            thisPageRef++;
        }
        pages->Release();
        thisDocPartUri->Release();
        doc->Release();
        thisDoc++;
    }

    docs->Release();
    docSeq->Release();

```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="d795e-133">Получить ресурсы части, связанные с этой страницей</span><span class="sxs-lookup"><span data-stu-id="d795e-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="d795e-134">В следующем примере кода возвращаются списки различных ресурсов, используемых этой страницей.</span><span class="sxs-lookup"><span data-stu-id="d795e-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );

    // use resources

    dictionaryResources->Release();
    imageResources->Release();
    fontResources->Release();
    colorProfileResources->Release();
    resources->Release();
```



 

