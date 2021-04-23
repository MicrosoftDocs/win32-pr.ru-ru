---
description: В этом разделе описывается использование интерфейсов, предоставляющих доступ к FixedDocumentSequence, который является верхним уровнем иерархии документов в OM-модели XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Работа с интерфейсами Икспсомдокументсекуенце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693176"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a><span data-ttu-id="f4ac9-103">Работа с интерфейсами Икспсомдокументсекуенце</span><span class="sxs-lookup"><span data-stu-id="f4ac9-103">Working with IXpsOMDocumentSequence Interfaces</span></span>

<span data-ttu-id="f4ac9-104">В этом разделе описывается использование интерфейсов, предоставляющих доступ к FixedDocumentSequence, который является верхним уровнем иерархии документов в OM-модели XPS.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-104">This topic describes how to use the interfaces that provide access to the FixedDocumentSequence, which is the top level of the document hierarchy in an XPS OM.</span></span>



| <span data-ttu-id="f4ac9-105">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="f4ac9-105">Interface name</span></span>                                                          | <span data-ttu-id="f4ac9-106">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f4ac9-106">Logical child interfaces</span></span>                            | <span data-ttu-id="f4ac9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f4ac9-107">Description</span></span>                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="f4ac9-108">**икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="f4ac9-108">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [<span data-ttu-id="f4ac9-109">**икспсомдокумент**</span><span class="sxs-lookup"><span data-stu-id="f4ac9-109">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | <span data-ttu-id="f4ac9-110">Группирует набор Фикседдокументс в упорядоченный список.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-110">Groups a set of FixedDocuments into an ordered list.</span></span><br/>          |
| [<span data-ttu-id="f4ac9-111">**икспсомдокументколлектион**</span><span class="sxs-lookup"><span data-stu-id="f4ac9-111">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | <span data-ttu-id="f4ac9-112">Нет</span><span class="sxs-lookup"><span data-stu-id="f4ac9-112">None</span></span><br/>                                     | <span data-ttu-id="f4ac9-113">Коллекция Фикседдокументс в последовательности документов XPS.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-113">The collection of FixedDocuments in an XPS document sequence.</span></span><br/> |



 

## <a name="code-example"></a><span data-ttu-id="f4ac9-114">Пример кода</span><span class="sxs-lookup"><span data-stu-id="f4ac9-114">Code Example</span></span>

<span data-ttu-id="f4ac9-115">В следующем примере кода получается указатель на интерфейс [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , содержащий последовательность документов объектной модели XPS, представленную *кспспаккаже*.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-115">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface that contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span> <span data-ttu-id="f4ac9-116">Затем в примере перечисляются документы в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f4ac9-116">The example then enumerates the documents in the collection.</span></span>


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



 

 




