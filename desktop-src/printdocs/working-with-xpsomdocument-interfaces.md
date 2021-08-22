---
description: В этом разделе описываются интерфейсы, обеспечивающие доступ к компонентам уровня документа в OM-модели XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Работа с интерфейсами Икспсомдокумент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7e8c0908382a731532f2697f03c8d67cb732ddf902f0c1ea181fe221d075fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033762"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>Работа с интерфейсами Икспсомдокумент

В этом разделе описываются интерфейсы, обеспечивающие доступ к компонентам уровня документа в OM-модели XPS.



| Имя интерфейса                                                                        | Логические дочерние интерфейсы                                      | Описание                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Представляет отдельную часть FixedDocument и привязывает коллекцию ссылок на страницы.<br/> [**Икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) — это интерфейс сбора, который используется для прохода по интерфейсам [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) в документе.<br/> |
| [**икспсомдокументструктурересаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | Нет<br/>                                               | Представляет часть Документструктуре.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>Примеры кода

В примерах кода в этом разделе показано, как некоторые интерфейсы документа используются в программе.

### <a name="get-the-page-references-of-a-document"></a>Получение ссылок на страницы документа

В следующем примере кода возвращается указатель на [**икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) , содержащий список интерфейсов [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) для документа, на который ссылается параметр *doc* .


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



### <a name="get-the-document-structure-of-a-document"></a>Получение структуры документа

В следующем примере кода возвращается ресурс, содержащий структуру документа.


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



 

 




