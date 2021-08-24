---
description: В этом разделе описывается использование интерфейсов, предоставляющих доступ к FixedDocumentSequence, который является верхним уровнем иерархии документов в OM-модели XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Работа с интерфейсами Икспсомдокументсекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edac74809de63c1ae4e688bb99214d11b091ee4e877c921e9280abc9c6868121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098666"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Работа с интерфейсами Икспсомдокументсекуенце

В этом разделе описывается использование интерфейсов, предоставляющих доступ к FixedDocumentSequence, который является верхним уровнем иерархии документов в OM-модели XPS.



| Имя интерфейса                                                          | Логические дочерние интерфейсы                            | Описание                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Группирует набор Фикседдокументс в упорядоченный список.<br/>          |
| [**икспсомдокументколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | Нет<br/>                                     | Коллекция Фикседдокументс в последовательности документов XPS.<br/> |



 

## <a name="code-example"></a>Пример кода

В следующем примере кода получается указатель на интерфейс [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , содержащий последовательность документов объектной модели XPS, представленную *кспспаккаже*. Затем в примере перечисляются документы в коллекции.


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 




