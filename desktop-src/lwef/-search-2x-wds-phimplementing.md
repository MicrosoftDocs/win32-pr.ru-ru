---
title: Реализация обработчика протокола для WDS
description: Создание обработчика протокола включает реализацию Исеарчпротокол для управления объектами Урлакцессор, Иурлакцессор для создания метаданных и для обнаружения соответствующих фильтров для элементов в хранилище данных, Ипротоколхандлерсите для создания экземпляра объекта Сеарчпротокол и для обнаружения соответствующих фильтров, а также для перечисления и фильтрации файлов, расположенных в иерархии.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133771"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="62807-103">Реализация обработчика протокола для WDS</span><span class="sxs-lookup"><span data-stu-id="62807-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="62807-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="62807-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="62807-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="62807-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="62807-106">Создание обработчика протокола включает реализацию [**исеарчпротокол**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) для управления объектами Урлакцессор, [**иурлакцессор**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) для создания метаданных и для обнаружения соответствующих фильтров для элементов в хранилище данных, ипротоколхандлерсите для создания экземпляра объекта сеарчпротокол и обнаружения соответствующих фильтров, а также [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)для фильтрации и фильтрации файлов, хранящихся в иерархическом виде.</span><span class="sxs-lookup"><span data-stu-id="62807-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="62807-107">Обработчик протокола должен быть многопоточным.</span><span class="sxs-lookup"><span data-stu-id="62807-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="62807-108">В этом разделе содержатся следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="62807-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="62807-109">Примечание по URL-адресам</span><span class="sxs-lookup"><span data-stu-id="62807-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="62807-110">Интерфейсы обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="62807-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="62807-111">Фильтры IFilter для контейнеров</span><span class="sxs-lookup"><span data-stu-id="62807-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="62807-112">Добавление функций параметров обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="62807-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="62807-113">исеарчпротоколоптионс</span><span class="sxs-lookup"><span data-stu-id="62807-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="62807-114">См. также</span><span class="sxs-lookup"><span data-stu-id="62807-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="62807-115">Примечание по URL-адресам</span><span class="sxs-lookup"><span data-stu-id="62807-115">Note on URLs</span></span>

<span data-ttu-id="62807-116">Microsoft Windows Desktop Search (WDS) использует URL-адреса для уникальной идентификации элементов в файловой системе, в хранилище, похожем на базу данных, или в Интернете.</span><span class="sxs-lookup"><span data-stu-id="62807-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="62807-117">URL-адрес, определяющий узел записи, называется начальной страницей. WDS начинается на этой начальной странице и рекурсивно выполняет обход хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="62807-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="62807-118">Типичная структура URL-адресов:</span><span class="sxs-lookup"><span data-stu-id="62807-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="62807-119">Чтобы добавить новое хранилище данных, необходимо выбрать имя, которое будет использоваться для его поиска, которое не конфликтует с текущими.</span><span class="sxs-lookup"><span data-stu-id="62807-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="62807-120">Мы рекомендуем использовать такое соглашение об именовании: companyName. Scheme.</span><span class="sxs-lookup"><span data-stu-id="62807-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="62807-121">Интерфейсы обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="62807-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="62807-122">**исеарчпротокол**</span><span class="sxs-lookup"><span data-stu-id="62807-122">**ISearchProtocol**</span></span>

<span data-ttu-id="62807-123">Интерфейс [**исеарчпротокол**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) вызывает, инициализирует и управляет объектами урлакцессор.</span><span class="sxs-lookup"><span data-stu-id="62807-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="62807-124">Дополнительные сведения о реализации интерфейса Исеарчпротокол см. в разделе **Справочник по интерфейсу исеарчпротокол**.</span><span class="sxs-lookup"><span data-stu-id="62807-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="62807-125">**иурлакцессор**</span><span class="sxs-lookup"><span data-stu-id="62807-125">**IUrlAccessor**</span></span>

<span data-ttu-id="62807-126">Для указанного URL-адреса интерфейс [**иурлакцессор**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) создает метаданные о структуре расположения и вложенных элементах, а также привязывает эти элементы к фильтру.</span><span class="sxs-lookup"><span data-stu-id="62807-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="62807-127">Экземпляр объекта **иурлакцессор** создается и инициализируется объектом сеарчпротокол. Однако можно также реализовать внутренний метод инициализации, чтобы объект **иурлакцессор** мог выполнять задачи инициализации, характерные для обработчика протокола, например проверку URL-адреса для элемента, к которому осуществляется доступ, или проверку времени последнего изменения, чтобы определить, должен ли файл обрабатываться в текущем сканировании.</span><span class="sxs-lookup"><span data-stu-id="62807-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="62807-128">Изменение времени для каталогов игнорируется.</span><span class="sxs-lookup"><span data-stu-id="62807-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="62807-129">Объект [**иурлакцессор**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) должен перечислить дочерние объекты, чтобы определить, были ли изменения или удаления.</span><span class="sxs-lookup"><span data-stu-id="62807-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="62807-130">Большая часть структуры объекта **урлакцессор** зависит от того, является ли структура иерархической или основанной на компоновке.</span><span class="sxs-lookup"><span data-stu-id="62807-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="62807-131">Для иерархических хранилищ данных объект **урлакцессор** должен найти фильтр, который может перечислить их содержимое.</span><span class="sxs-lookup"><span data-stu-id="62807-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="62807-132">Еще одно различие между иерархическими и обработчиками протоколов на основе ссылок заключается в использовании метода DataDirectory.</span><span class="sxs-lookup"><span data-stu-id="62807-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="62807-133">В обработчиках протоколов на основе связей этот метод должен возвращать \_ значение S false.</span><span class="sxs-lookup"><span data-stu-id="62807-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="62807-134">Обработчики иерархических протоколов должны возвращать значения S \_ ОК для контейнеров.</span><span class="sxs-lookup"><span data-stu-id="62807-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="62807-135">Дополнительные инструкции по реализации интерфейса [**иурлакцессор**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) см. в справочнике по [**интерфейсу иурлакцессор**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .</span><span class="sxs-lookup"><span data-stu-id="62807-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="62807-136">**ипротоколхандлерсите**</span><span class="sxs-lookup"><span data-stu-id="62807-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="62807-137">Этот интерфейс используется для создания экземпляра объекта **сеарчпротокол** , а также предоставляет объект **урлакцессор** с соответствующим фильтром для УКАЗАННОГО идентификатора класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="62807-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="62807-138">Фильтры IFilter для контейнеров</span><span class="sxs-lookup"><span data-stu-id="62807-138">IFilters for Containers</span></span>

<span data-ttu-id="62807-139">При реализации иерархического обработчика протокола необходимо реализовать компонент контейнера [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter), который перечисляет URL-адреса, представляющие контейнеры или папки.</span><span class="sxs-lookup"><span data-stu-id="62807-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="62807-140">Процесс перечисления — это цикл по методам **noreturn и** **GetValue** интерфейса IFilter, которые возвращают список URL-адресов, представляющих каждый элемент в контейнере.</span><span class="sxs-lookup"><span data-stu-id="62807-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="62807-141">Во-первых, функция **фуллпроспек возвращает объект** с набором свойств Set \_ proping и либо:</span><span class="sxs-lookup"><span data-stu-id="62807-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="62807-142">PID \_ ГСР \_ дирлинк, URL-адрес элемента без времени последнего изменения или</span><span class="sxs-lookup"><span data-stu-id="62807-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="62807-143">PID \_ ГСР \_ дирлинк \_ со \_ временем, URL-адрес и время последнего изменения</span><span class="sxs-lookup"><span data-stu-id="62807-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="62807-144">Набор свойств GUID для набора \_ PROPS — 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span><span class="sxs-lookup"><span data-stu-id="62807-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="62807-145">Свойство ПРОПСПЕК имеет значение PID \_ ГСР \_ дирлинк = 2 или PID \_ ГСР \_ дирлинк \_ с параметром \_ time = 12 Decimal.</span><span class="sxs-lookup"><span data-stu-id="62807-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="62807-146">Возврат PID \_ ГСР \_ дирлинк \_ со \_ временем более эффективен, так как индексатор может немедленно определить, нужно ли индексировать элемент, не вызывая методы исеарчпротокол->Креатеурлакцессор () и иурлакцессор->жетластмодифиед ().</span><span class="sxs-lookup"><span data-stu-id="62807-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="62807-147">Затем функция **GetValue** возвращает пропвариант для URL-адреса (и время последнего изменения, если используется):</span><span class="sxs-lookup"><span data-stu-id="62807-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="62807-148">VT \_ LPWSTR, URL-адрес дочернего элемента или</span><span class="sxs-lookup"><span data-stu-id="62807-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="62807-149">Вектор URL-адреса, за которым следует FILETIME</span><span class="sxs-lookup"><span data-stu-id="62807-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="62807-150">В следующем примере кода показано, как создать правильный PID \_ ГСР \_ дирлинк \_ со \_ временем.</span><span class="sxs-lookup"><span data-stu-id="62807-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="62807-151">**ЭТОТ КОД И ИНФОРМАЦИЯ ПРЕДОСТАВЛЯЮТСЯ "КАК ЕСТЬ" БЕЗ КАКИХ-ЛИБО ЯВНЫХ ИЛИ ПОДРАЗУМЕВАЕМЫХ ГАРАНТИЙ, ВКЛЮЧАЯ, НО НЕ ОГРАНИЧИВАЯСЬ ПОДРАЗУМЕВАЕМЫМИ ГАРАНТИЯМИ ПРИГОДНОСТИ И (ИЛИ) ПРИГОДНОСТИ ДЛЯ КОНКРЕТНОЙ ЦЕЛИ.**</span><span class="sxs-lookup"><span data-stu-id="62807-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="62807-152">(C) корпорация Майкрософт (Microsoft Corporation).</span><span class="sxs-lookup"><span data-stu-id="62807-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="62807-153">Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="62807-153">All rights reserved.</span></span>

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]
>
> <span data-ttu-id="62807-154">Компоненту [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)контейнера всегда следует перечислять все дочерние URL-адреса, даже если дочерние URL-адреса не изменялись, так как индексатор обнаруживает удаления с помощью процесса перечисления.</span><span class="sxs-lookup"><span data-stu-id="62807-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="62807-155">Если Дата вывода в папке DIR \_ \_ со \_ временем указывает на то, что данные не изменялись, индексатор не обновляет данные для этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="62807-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="62807-156">Физический URL-адрес — это URL-адрес, обрабатываемый объектом **урлакцессор** .</span><span class="sxs-lookup"><span data-stu-id="62807-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="62807-157">Если фильтр не создает понятный Дисплайурл, WDS Отображает физический URL-адрес пользователя как часть результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="62807-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="62807-158">Схема WDS содержит два свойства для управления отображением конечного пользователя, как показано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="62807-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="62807-159">Код GUID</span><span class="sxs-lookup"><span data-stu-id="62807-159">GUID</span></span>                                 | <span data-ttu-id="62807-160">пропспек</span><span class="sxs-lookup"><span data-stu-id="62807-160">PROPSPEC</span></span>      | <span data-ttu-id="62807-161">Описание</span><span class="sxs-lookup"><span data-stu-id="62807-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="62807-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="62807-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="62807-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="62807-163">DisplayFolder</span></span> | <span data-ttu-id="62807-164">Путь к папке, отображаемый пользователю в результатах поиска</span><span class="sxs-lookup"><span data-stu-id="62807-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="62807-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="62807-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="62807-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="62807-166">FolderName</span></span>    | <span data-ttu-id="62807-167">Отображаемое имя родительской папки</span><span class="sxs-lookup"><span data-stu-id="62807-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="62807-168">Если код не создает DisplayFolder или имя_папки, эти значения вычисляются из Дисплайурл.</span><span class="sxs-lookup"><span data-stu-id="62807-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="62807-169">Косые черты в контейнерах URL-адреса указываются в хранилище или файловой системе.</span><span class="sxs-lookup"><span data-stu-id="62807-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="62807-170">Добавление функций параметров обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="62807-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="62807-171">Чтобы обработчик протокола имел начальную страницу по умолчанию (и URL-адрес узла входа), необходимо реализовать интерфейс **исеарчпротоколоптионс** .</span><span class="sxs-lookup"><span data-stu-id="62807-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="62807-172">В будущих версиях WDS этот интерфейс будет предоставлять обработчики диалогового окна Параметры для улучшения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62807-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="62807-173">Этот интерфейс обеспечивает следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="62807-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="62807-174">Определяет, выполняются ли требования для обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="62807-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="62807-175">Например, хранилище обработчика протокола может требовать доступ к конкретному приложению для правильного индексирования данных приложения, но это приложение недоступно.</span><span class="sxs-lookup"><span data-stu-id="62807-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="62807-176">Определяет минимальные требования, необходимые обработчику протокола для обработки элемента.</span><span class="sxs-lookup"><span data-stu-id="62807-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="62807-177">Требования могут быть выражены с помощью понятного, локализованного описания, например Microsoft Outlook 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="62807-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="62807-178">Определяет URL-адреса, которые обработчик протокола должен обработать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62807-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="62807-179">исеарчпротоколоптионс</span><span class="sxs-lookup"><span data-stu-id="62807-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="62807-180">В следующей таблице описаны методы, которые необходимо реализовать для интерфейса **исеарчпротоколоптионс** .</span><span class="sxs-lookup"><span data-stu-id="62807-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="62807-181">Метод</span><span class="sxs-lookup"><span data-stu-id="62807-181">Method</span></span>               | <span data-ttu-id="62807-182">Описание</span><span class="sxs-lookup"><span data-stu-id="62807-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62807-183">чеккрекуирементс</span><span class="sxs-lookup"><span data-stu-id="62807-183">CheckRequirements</span></span>    | <span data-ttu-id="62807-184">Определяет, выполняются ли минимальные требования пользовательского обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="62807-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="62807-185">жетдефаулткравлскопе</span><span class="sxs-lookup"><span data-stu-id="62807-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="62807-186">Возвращает список URL-адресов по умолчанию в указанном хранилище для пользовательского обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="62807-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="62807-187">Требования</span><span class="sxs-lookup"><span data-stu-id="62807-187">GetRequirements</span></span>      | <span data-ttu-id="62807-188">Определяет понятное для пользователя локализованное описание минимальных требований для пользовательского обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="62807-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="62807-189">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="62807-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62807-190">**Reference**</span><span class="sxs-lookup"><span data-stu-id="62807-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62807-191">Уведомление индекса изменений</span><span class="sxs-lookup"><span data-stu-id="62807-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="62807-192">Добавление значков, предварительных версий и контекстных меню с расширениями оболочки</span><span class="sxs-lookup"><span data-stu-id="62807-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="62807-193">Установка и регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="62807-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 