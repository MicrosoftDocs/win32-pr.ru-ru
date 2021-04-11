---
description: В этом разделе описывается использование интерфейсов, предоставляющих доступ к ссылкам на страницы в OM-модели XPS.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Работа с интерфейсами Икспсомпажереференце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910483"
---
# <a name="working-with-ixpsompagereference-interfaces"></a>Работа с интерфейсами Икспсомпажереференце

В этом разделе описывается использование интерфейсов, предоставляющих доступ к ссылкам на страницы в OM-модели XPS.



| Имя интерфейса                                                  | Логические дочерние интерфейсы                    | Описание                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | Виртуализация содержимого страницы документа. <br/> Ссылка на страницу содержит основные сведения о странице, некоторые свойства страницы и ссылку на содержимое страницы. Интерфейс [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , который состоит из содержимого страницы, возвращается методом [**Икспсомпажереференце::-Page**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .<br/> |
| [**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | Нет<br/>                             | Содержит список элементов страницы, которые являются объектами гиперссылок. Список возвращается методом [**икспсомпажереференце:: коллектлинктаржетс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .<br/>                                                                                                                                                               |
| [**икспсомпартресаурцес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | Нет<br/>                             | Содержит список ресурсов на основе части, связанных со страницей. Этот список возвращается методом [**икспсомпажереференце:: коллектпартресаурцес**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .<br/>                                                                                                                                     |



 

## <a name="code-examples"></a>Примеры кода

В следующих примерах кода показано, как работать со справочными интерфейсами страницы в программе.

-   [Получение содержимого страницы](#get-the-page-contents)
-   [Получить список конечных объектов гиперссылок на этой странице](#get-the-list-of-hyperlink-targets-on-this-page)
-   [Получить ресурсы части, связанные с этой страницей](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a>Получение содержимого страницы

В следующем примере кода возвращается указатель на интерфейс [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , который состоит из содержимого страницы. Если страница не была загружена в модель XPS, как это происходит при инициализации модели XPS с помощью вызова [**икспсомобжектфактори:: креатепаккажефромфиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), вызов [**Икспсомпажереференце::-Page**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) приведет к загрузке страницы в объектную модель XPS.


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a>Получить список конечных объектов гиперссылок на этой странице

В следующем примере кода возвращается указатель на интерфейс [**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) , содержащий список элементов страницы, которые являются объектами гиперссылок. Если страница не загружена в модель XPS, список целевых объектов гиперссылки считывается из разметки **PageContent. линктаржетс** . Если страница загружена, [**коллектлинктаржетс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) проверяет каждый элемент на странице и возвращает список элементов, атрибут **Ишиперлинктаржет** которых имеет **значение true**.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Получить ресурсы части, связанные с этой страницей

В следующем примере кода возвращаются списки различных ресурсов, используемых этой страницей.


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
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**икспсомпартресаурцес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




