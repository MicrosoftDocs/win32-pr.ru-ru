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
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="63427-103">Работа с интерфейсами Икспсомпажереференце</span><span class="sxs-lookup"><span data-stu-id="63427-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="63427-104">В этом разделе описывается использование интерфейсов, предоставляющих доступ к ссылкам на страницы в OM-модели XPS.</span><span class="sxs-lookup"><span data-stu-id="63427-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="63427-105">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="63427-105">Interface name</span></span>                                                  | <span data-ttu-id="63427-106">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="63427-106">Logical child interfaces</span></span>                    | <span data-ttu-id="63427-107">Описание</span><span class="sxs-lookup"><span data-stu-id="63427-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63427-108">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="63427-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="63427-109">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="63427-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="63427-110">Виртуализация содержимого страницы документа.</span><span class="sxs-lookup"><span data-stu-id="63427-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="63427-111">Ссылка на страницу содержит основные сведения о странице, некоторые свойства страницы и ссылку на содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="63427-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="63427-112">Интерфейс [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , который состоит из содержимого страницы, возвращается методом [**Икспсомпажереференце::-Page**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .</span><span class="sxs-lookup"><span data-stu-id="63427-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="63427-113">**икспсомнамеколлектион**</span><span class="sxs-lookup"><span data-stu-id="63427-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="63427-114">Нет</span><span class="sxs-lookup"><span data-stu-id="63427-114">None</span></span><br/>                             | <span data-ttu-id="63427-115">Содержит список элементов страницы, которые являются объектами гиперссылок.</span><span class="sxs-lookup"><span data-stu-id="63427-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="63427-116">Список возвращается методом [**икспсомпажереференце:: коллектлинктаржетс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .</span><span class="sxs-lookup"><span data-stu-id="63427-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="63427-117">**икспсомпартресаурцес**</span><span class="sxs-lookup"><span data-stu-id="63427-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="63427-118">Нет</span><span class="sxs-lookup"><span data-stu-id="63427-118">None</span></span><br/>                             | <span data-ttu-id="63427-119">Содержит список ресурсов на основе части, связанных со страницей.</span><span class="sxs-lookup"><span data-stu-id="63427-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="63427-120">Этот список возвращается методом [**икспсомпажереференце:: коллектпартресаурцес**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .</span><span class="sxs-lookup"><span data-stu-id="63427-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="63427-121">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="63427-121">Code Examples</span></span>

<span data-ttu-id="63427-122">В следующих примерах кода показано, как работать со справочными интерфейсами страницы в программе.</span><span class="sxs-lookup"><span data-stu-id="63427-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="63427-123">Получение содержимого страницы</span><span class="sxs-lookup"><span data-stu-id="63427-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="63427-124">Получить список конечных объектов гиперссылок на этой странице</span><span class="sxs-lookup"><span data-stu-id="63427-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="63427-125">Получить ресурсы части, связанные с этой страницей</span><span class="sxs-lookup"><span data-stu-id="63427-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="63427-126">Получение содержимого страницы</span><span class="sxs-lookup"><span data-stu-id="63427-126">Get the page contents</span></span>

<span data-ttu-id="63427-127">В следующем примере кода возвращается указатель на интерфейс [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , который состоит из содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="63427-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="63427-128">Если страница не была загружена в модель XPS, как это происходит при инициализации модели XPS с помощью вызова [**икспсомобжектфактори:: креатепаккажефромфиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), вызов [**Икспсомпажереференце::-Page**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) приведет к загрузке страницы в объектную модель XPS.</span><span class="sxs-lookup"><span data-stu-id="63427-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="63427-129">Получить список конечных объектов гиперссылок на этой странице</span><span class="sxs-lookup"><span data-stu-id="63427-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="63427-130">В следующем примере кода возвращается указатель на интерфейс [**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) , содержащий список элементов страницы, которые являются объектами гиперссылок.</span><span class="sxs-lookup"><span data-stu-id="63427-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="63427-131">Если страница не загружена в модель XPS, список целевых объектов гиперссылки считывается из разметки **PageContent. линктаржетс** .</span><span class="sxs-lookup"><span data-stu-id="63427-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="63427-132">Если страница загружена, [**коллектлинктаржетс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) проверяет каждый элемент на странице и возвращает список элементов, атрибут **Ишиперлинктаржет** которых имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="63427-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="63427-133">Получить ресурсы части, связанные с этой страницей</span><span class="sxs-lookup"><span data-stu-id="63427-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="63427-134">В следующем примере кода возвращаются списки различных ресурсов, используемых этой страницей.</span><span class="sxs-lookup"><span data-stu-id="63427-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="63427-135">См. также</span><span class="sxs-lookup"><span data-stu-id="63427-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63427-136">**икспсомнамеколлектион**</span><span class="sxs-lookup"><span data-stu-id="63427-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="63427-137">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="63427-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="63427-138">**икспсомпажереференце**</span><span class="sxs-lookup"><span data-stu-id="63427-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="63427-139">**икспсомпартресаурцес**</span><span class="sxs-lookup"><span data-stu-id="63427-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="63427-140">XPS</span><span class="sxs-lookup"><span data-stu-id="63427-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




