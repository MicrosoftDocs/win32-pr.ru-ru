---
description: В этом разделе описываются интерфейсы, обеспечивающие доступ к компонентам уровня документа в OM-модели XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Работа с интерфейсами Икспсомдокумент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693032"
---
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="d47d8-103">Работа с интерфейсами Икспсомдокумент</span><span class="sxs-lookup"><span data-stu-id="d47d8-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="d47d8-104">В этом разделе описываются интерфейсы, обеспечивающие доступ к компонентам уровня документа в OM-модели XPS.</span><span class="sxs-lookup"><span data-stu-id="d47d8-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="d47d8-105">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="d47d8-105">Interface name</span></span>                                                                        | <span data-ttu-id="d47d8-106">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="d47d8-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="d47d8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d47d8-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47d8-108">**икспсомдокумент**</span><span class="sxs-lookup"><span data-stu-id="d47d8-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="d47d8-109">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="d47d8-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="d47d8-110">Представляет отдельную часть FixedDocument и привязывает коллекцию ссылок на страницы.</span><span class="sxs-lookup"><span data-stu-id="d47d8-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="d47d8-111">[**Икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) — это интерфейс сбора, который используется для прохода по интерфейсам [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) в документе.</span><span class="sxs-lookup"><span data-stu-id="d47d8-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="d47d8-112">**икспсомдокументструктурересаурце**</span><span class="sxs-lookup"><span data-stu-id="d47d8-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="d47d8-113">Нет</span><span class="sxs-lookup"><span data-stu-id="d47d8-113">None</span></span><br/>                                               | <span data-ttu-id="d47d8-114">Представляет часть Документструктуре.</span><span class="sxs-lookup"><span data-stu-id="d47d8-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="d47d8-115">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="d47d8-115">Code Examples</span></span>

<span data-ttu-id="d47d8-116">В примерах кода в этом разделе показано, как некоторые интерфейсы документа используются в программе.</span><span class="sxs-lookup"><span data-stu-id="d47d8-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="d47d8-117">Получение ссылок на страницы документа</span><span class="sxs-lookup"><span data-stu-id="d47d8-117">Get the page references of a document</span></span>

<span data-ttu-id="d47d8-118">В следующем примере кода возвращается указатель на [**икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) , содержащий список интерфейсов [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) для документа, на который ссылается параметр *doc* .</span><span class="sxs-lookup"><span data-stu-id="d47d8-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="d47d8-119">Получение структуры документа</span><span class="sxs-lookup"><span data-stu-id="d47d8-119">Get the document structure of a document</span></span>

<span data-ttu-id="d47d8-120">В следующем примере кода возвращается ресурс, содержащий структуру документа.</span><span class="sxs-lookup"><span data-stu-id="d47d8-120">The following code example gets the resource that contains the document structure.</span></span>


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




