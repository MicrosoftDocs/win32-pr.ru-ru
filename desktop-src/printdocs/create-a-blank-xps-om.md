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
# <a name="create-a-blank-xps-om"></a>Создание пустой объектной модели XPS

В этом разделе описывается создание пустой модели XPS. В нем представлены примеры кода, иллюстрирующие использование OM XPS для создания структуры документа XPS-документа с одной пустой страницей.

Для сохранения в виде документа XPS необходимо по крайней мере следующие компоненты:

-   [**Икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , описывающий пакет документа XPS
-   Объект [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , содержащий структуру содержимого пакета.
-   Объект [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) , содержащий платформу документа в пакете
-   Объект [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) , содержащий коллекцию страниц в документе
-   Объект [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , содержащий пустую страницу

При использовании этих интерфейсов объектная модель XPS будет содержать документ с одной пустой страницей. Чтобы создать этот документ в объектной модели XPS, программа должна сначала создать отдельные компоненты, а затем связать их вместе.

Перед использованием приведенных ниже примеров кода прочитайте заявление об отказе в [распространенных задачах программирования документов XPS](common-xps-document-tasks.md).

## <a name="code-examples"></a>Примеры кода

В следующем примере кода предполагается, что инициализация, описанная в разделе [Инициализация объектной модели XPS](xps-object-model-initialization.md), прошла успешно.


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



## <a name="best-practices"></a>Рекомендации

После того как вы использовали интерфейс [**иопкпартури**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) для создания компонента (например, после вызова метода **CreateDocument** в примере кода), отпустите указатель на этот интерфейс, если это не требуется для другого вызова.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Навигация по OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Запись текста в объектную модель XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Рисование графики в OM-объекте XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Размещение изображений в объектной модели XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Используется на этой странице**
</dt> <dt>

[**иопкпартури**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**икспсомдокументколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**\_Размер XPS**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Инициализация объектной модели XPS](xps-object-model-initialization.md)
</dt> <dt>

[API для упаковки](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Справочник по API документов XPS](xps-programming-reference.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
