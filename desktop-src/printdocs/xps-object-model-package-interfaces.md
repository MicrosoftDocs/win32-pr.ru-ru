---
description: Интерфейсы пакета представляют верхний уровень модели XPS, соответствующий файлу документа XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Интерфейсы пакета OM в XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6732531e3874046bbd174c363db24e304da95b9596b810014abb52a795e720c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886144"
---
# <a name="xps-om-package-interfaces"></a>Интерфейсы пакета OM в XPS

Интерфейсы пакета представляют верхний уровень модели XPS, соответствующий файлу документа XPS. Эти интерфейсы содержат методы сериализации OM XPS в документ или поток XPS, а также десериализация пакета XPS для создания объектной модели XPS, которая позволяет программе получать доступ к содержимому документа.



| Имя интерфейса                                                  | Логические дочерние интерфейсы                                                                                                            | Описание                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**икспсомкорепропертиес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Полная модель XPS, соответствующая пакету, содержащему документ XPS.<br/> |
| [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | Нет<br/>                                                                                                                     | Включает добавочную сериализацию страниц документа в пакет.<br/>                   |
| [**икспсомкорепропертиес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Нет<br/>                                                                                                                     | Обращается к метаданным документа. <br/>                                                    |



 

## <a name="code-examples"></a>Примеры кода

В приведенных ниже примерах кода показано, как некоторые интерфейсы пакета используются программой. Если не указано иное, все курсивные элементы являются именами параметров.

-   [Чтение XPS-документа в объектную модель XPS](#read-an-xps-document-into-an-xps-om)
-   [Запись объектной модели XPS в файл документа XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Доступ к последовательности документов объектной модели XPS](#access-the-document-sequence-of-the-xps-om)
-   [Доступ к Корепропертиесу документа](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Чтение XPS-документа в объектную модель XPS

Из существующего документа XPS, имя файла которого хранится в *кспсдокументфиленаме*, этот пример кода создает объектную модель XPS, на которую ссылается *кспспаккаже*.


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Запись объектной модели XPS в файл документа XPS

В следующем примере кода показана запись объектной модели XPS, на которую ссылается *кспспаккаже*. В примере создается документ XPS в файле, имя которого хранится в *filename*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Доступ к последовательности документов объектной модели XPS

В следующем примере кода получается указатель на интерфейс [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , который содержит последовательность документов объектной модели XPS, представленную *кспспаккаже*.


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



### <a name="access-the-documents-coreproperties"></a>Доступ к Корепропертиесу документа

В следующем примере кода получается указатель на интерфейс [**икспсомкорепропертиес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , который позволяет программе получить доступ к содержимому части корепропертиес. В этом примере предполагается, что документ был прочитан в объектную модель XPS, представленную *кспспаккаже*.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование интерфейса Икспсомпаккажевритер](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Навигация по OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[**Интерфейс Икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Интерфейс Икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Интерфейс Икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Интерфейс Икспсомкорепропертиес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




