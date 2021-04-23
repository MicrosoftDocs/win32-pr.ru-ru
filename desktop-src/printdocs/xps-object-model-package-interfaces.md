---
description: Интерфейсы пакета представляют верхний уровень модели XPS, соответствующий файлу документа XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Интерфейсы пакета OM в XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898685"
---
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="561a0-103">Интерфейсы пакета OM в XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="561a0-104">Интерфейсы пакета представляют верхний уровень модели XPS, соответствующий файлу документа XPS.</span><span class="sxs-lookup"><span data-stu-id="561a0-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="561a0-105">Эти интерфейсы содержат методы сериализации OM XPS в документ или поток XPS, а также десериализация пакета XPS для создания объектной модели XPS, которая позволяет программе получать доступ к содержимому документа.</span><span class="sxs-lookup"><span data-stu-id="561a0-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="561a0-106">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="561a0-106">Interface name</span></span>                                                  | <span data-ttu-id="561a0-107">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="561a0-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="561a0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="561a0-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="561a0-109">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="561a0-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="561a0-110">**икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="561a0-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="561a0-111">**икспсомкорепропертиес**</span><span class="sxs-lookup"><span data-stu-id="561a0-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="561a0-112">Полная модель XPS, соответствующая пакету, содержащему документ XPS.</span><span class="sxs-lookup"><span data-stu-id="561a0-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="561a0-113">**икспсомпаккажевритер**</span><span class="sxs-lookup"><span data-stu-id="561a0-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="561a0-114">Нет</span><span class="sxs-lookup"><span data-stu-id="561a0-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="561a0-115">Включает добавочную сериализацию страниц документа в пакет.</span><span class="sxs-lookup"><span data-stu-id="561a0-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="561a0-116">**икспсомкорепропертиес**</span><span class="sxs-lookup"><span data-stu-id="561a0-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="561a0-117">Нет</span><span class="sxs-lookup"><span data-stu-id="561a0-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="561a0-118">Обращается к метаданным документа.</span><span class="sxs-lookup"><span data-stu-id="561a0-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="561a0-119">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="561a0-119">Code Examples</span></span>

<span data-ttu-id="561a0-120">В приведенных ниже примерах кода показано, как некоторые интерфейсы пакета используются программой.</span><span class="sxs-lookup"><span data-stu-id="561a0-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="561a0-121">Если не указано иное, все курсивные элементы являются именами параметров.</span><span class="sxs-lookup"><span data-stu-id="561a0-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="561a0-122">Чтение XPS-документа в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="561a0-123">Запись объектной модели XPS в файл документа XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="561a0-124">Доступ к последовательности документов объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="561a0-125">Доступ к Корепропертиесу документа</span><span class="sxs-lookup"><span data-stu-id="561a0-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="561a0-126">Чтение XPS-документа в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="561a0-127">Из существующего документа XPS, имя файла которого хранится в *кспсдокументфиленаме*, этот пример кода создает объектную модель XPS, на которую ссылается *кспспаккаже*.</span><span class="sxs-lookup"><span data-stu-id="561a0-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="561a0-128">Запись объектной модели XPS в файл документа XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="561a0-129">В следующем примере кода показана запись объектной модели XPS, на которую ссылается *кспспаккаже*.</span><span class="sxs-lookup"><span data-stu-id="561a0-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="561a0-130">В примере создается документ XPS в файле, имя которого хранится в *filename*.</span><span class="sxs-lookup"><span data-stu-id="561a0-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="561a0-131">Доступ к последовательности документов объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="561a0-132">В следующем примере кода получается указатель на интерфейс [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , который содержит последовательность документов объектной модели XPS, представленную *кспспаккаже*.</span><span class="sxs-lookup"><span data-stu-id="561a0-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="561a0-133">Доступ к Корепропертиесу документа</span><span class="sxs-lookup"><span data-stu-id="561a0-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="561a0-134">В следующем примере кода получается указатель на интерфейс [**икспсомкорепропертиес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , который позволяет программе получить доступ к содержимому части корепропертиес.</span><span class="sxs-lookup"><span data-stu-id="561a0-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="561a0-135">В этом примере предполагается, что документ был прочитан в объектную модель XPS, представленную *кспспаккаже*.</span><span class="sxs-lookup"><span data-stu-id="561a0-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a><span data-ttu-id="561a0-136">См. также</span><span class="sxs-lookup"><span data-stu-id="561a0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="561a0-137">Использование интерфейса Икспсомпаккажевритер</span><span class="sxs-lookup"><span data-stu-id="561a0-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="561a0-138">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="561a0-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="561a0-139">**Интерфейс Икспсомдокументсекуенце**</span><span class="sxs-lookup"><span data-stu-id="561a0-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="561a0-140">**Интерфейс Икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="561a0-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="561a0-141">**Интерфейс Икспсомпаккажевритер**</span><span class="sxs-lookup"><span data-stu-id="561a0-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="561a0-142">**Интерфейс Икспсомкорепропертиес**</span><span class="sxs-lookup"><span data-stu-id="561a0-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




