---
description: Описание создания файла описания OpenSearch (. OSDX-) для подключения внешних хранилищ данных к клиенту Windows через протокол OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Создание файла описания OpenSearch в федеративного поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990971"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="b2d3f-103">Создание файла описания OpenSearch в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="b2d3f-104">Описание создания файла описания OpenSearch (. OSDX-) для подключения внешних хранилищ данных к клиенту Windows через протокол [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="b2d3f-105">Федеративный поиск позволяет пользователям выполнять поиск в удаленном хранилище данных и просматривать результаты в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="b2d3f-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b2d3f-107">Файл описания OpenSearch</span><span class="sxs-lookup"><span data-stu-id="b2d3f-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="b2d3f-108">Минимальная обязательные дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b2d3f-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="b2d3f-109">Стандартные элементы в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="b2d3f-110">ShortName</span><span class="sxs-lookup"><span data-stu-id="b2d3f-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="b2d3f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b2d3f-111">Description</span></span>](#description)
    -   [<span data-ttu-id="b2d3f-112">Шаблон URL-адреса для результатов RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="b2d3f-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="b2d3f-113">Шаблон URL-адреса для результатов в Интернете</span><span class="sxs-lookup"><span data-stu-id="b2d3f-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="b2d3f-114">Параметры шаблона URL-адреса</span><span class="sxs-lookup"><span data-stu-id="b2d3f-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="b2d3f-115">Страничные результаты</span><span class="sxs-lookup"><span data-stu-id="b2d3f-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="b2d3f-116">Разбиение на страницы с помощью индекса элемента</span><span class="sxs-lookup"><span data-stu-id="b2d3f-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="b2d3f-117">Разбиение на страницы с помощью индекса страниц</span><span class="sxs-lookup"><span data-stu-id="b2d3f-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="b2d3f-118">Page Size</span><span class="sxs-lookup"><span data-stu-id="b2d3f-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="b2d3f-119">Расширенные элементы в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="b2d3f-120">Максимальное число результатов</span><span class="sxs-lookup"><span data-stu-id="b2d3f-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="b2d3f-121">Сопоставление свойств</span><span class="sxs-lookup"><span data-stu-id="b2d3f-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="b2d3f-122">Предварительные версии</span><span class="sxs-lookup"><span data-stu-id="b2d3f-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="b2d3f-123">Открыть пункт меню "расположение файла"</span><span class="sxs-lookup"><span data-stu-id="b2d3f-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="b2d3f-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b2d3f-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b2d3f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b2d3f-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="b2d3f-126">Файл описания OpenSearch</span><span class="sxs-lookup"><span data-stu-id="b2d3f-126">OpenSearch Description File</span></span>

<span data-ttu-id="b2d3f-127">Файл описания OpenSearch (. OSDX-) для федеративного поиска Windows должен соблюдать следующие правила.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="b2d3f-128">Быть допустимым документом описания OpenSearch, как определено в спецификации [OpenSearch](https://github.com/dewitt/opensearch) 1,1.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="b2d3f-129">Укажите шаблон URL-адреса с типом формата RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="b2d3f-130">Используйте расширение имени файла OSDX-или сопоставлено с расширением имени файла OSDX-при скачивании из Интернета.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="b2d3f-131">Например, сервер не обязательно должен использовать. OSDX-.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="b2d3f-132">Сервер может возвратить файл с любым расширением файла, например. XML, и обрабатываться так, как если бы он был OSDX--файлом, если он использует правильный тип MIME для документов описания OpenSearch (OSDX--файлов).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="b2d3f-133">Укажите значение элемента **ShortName** (рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="b2d3f-134">Минимальная обязательные дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b2d3f-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="b2d3f-135">В следующем примере файл. OSDX-состоит из параметра **ShortName** и `Url` элементов, которые являются минимально необходимыми дочерними элементами.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="b2d3f-136">Стандартные элементы в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="b2d3f-137">В дополнение к минимальным дочерним элементам, федеративный поиск поддерживает следующие стандартные элементы.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="b2d3f-138">ShortName</span><span class="sxs-lookup"><span data-stu-id="b2d3f-138">Shortname</span></span>

<span data-ttu-id="b2d3f-139">Windows использует значение элемента **ShortName** для именования файла. сеарчконнектор-MS (поискового соединителя), который создается, когда пользователь открывает файл OSDX-.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="b2d3f-140">Windows гарантирует, что созданное имя файла будет использовать только символы, разрешенные в именах файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="b2d3f-141">Если значение параметра **ShortName** не указано, файл. сеарчконнектор-MS пытается использовать вместо него имя файла OSDX-.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="b2d3f-142">В следующем коде показано, как использовать элемент **ShortName** в файле с расширением OSDX-.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="b2d3f-143">Описание</span><span class="sxs-lookup"><span data-stu-id="b2d3f-143">Description</span></span>

<span data-ttu-id="b2d3f-144">Windows использует значение элемента **Description** для заполнения описания файла, отображаемого в области Подробности проводника Windows, когда пользователь выбирает файл сеарчконнектор-MS.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="b2d3f-145">Шаблон URL-адреса для результатов RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="b2d3f-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="b2d3f-146">Файл. OSDX-должен включать один элемент **формата URL** и атрибут **шаблона** (шаблон URL-адреса), который ВОЗВРАЩАЕТ результаты в формате RSS или Atom.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="b2d3f-147">Атрибуту format необходимо присвоить значение `application/rss+xml` для отформатированных результатов RSS или `application/atom+xml` для отформатированных результатов Atom, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="b2d3f-148">Элемент **форматирования URL-адреса** и атрибут **шаблона** обычно НАЗЫВАЮТСЯ шаблоном URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="b2d3f-149">Шаблон URL-адреса для результатов в Интернете</span><span class="sxs-lookup"><span data-stu-id="b2d3f-149">URL Template for web Results</span></span>

<span data-ttu-id="b2d3f-150">Если существует версия результатов поиска, которую можно просмотреть в веб-браузере, необходимо предоставить **URL-адрес формата** , `text/html` элемент и атрибут **шаблона** , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="b2d3f-151">Если указать элемент **URL Format = "text/html"** и атрибут **шаблона** , в командной строке проводника Windows появится кнопка, как показано на следующем снимке экрана, которая позволяет пользователю открывать веб-браузер для просмотра результатов поиска при выполнении запроса пользователем.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![снимок экрана, показывающий кнопку перехода по веб-поиску.](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="b2d3f-153">Откат запроса к веб-ИНТЕРФЕЙСу хранилища данных важен в некоторых сценариях.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="b2d3f-154">Например, пользователю может потребоваться просмотреть более 100 результатов (по умолчанию число элементов, запрашиваемых поставщиком OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="b2d3f-155">Если да, то пользователь может также использовать функции поиска, доступные только на веб-сайте хранилища данных, например повторное выполнение запросов с другим порядком сортировки или сведение и фильтрация запроса с помощью связанных метаданных.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="b2d3f-156">Параметры шаблона URL-адреса</span><span class="sxs-lookup"><span data-stu-id="b2d3f-156">URL Template Parameters</span></span>

<span data-ttu-id="b2d3f-157">Поставщик OpenSearch всегда выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="b2d3f-158">Использует шаблон URL-адреса для отправки запроса веб-службе.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="b2d3f-159">Пытается заменить токены, найденные в шаблоне URL, перед отправкой запроса веб-службе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="b2d3f-160">Заменяет стандартные токены OpenSearch, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="b2d3f-161">Удаляет все токены, которые не перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="b2d3f-162">Поддерживаемый токен</span><span class="sxs-lookup"><span data-stu-id="b2d3f-162">Supported token</span></span>  | <span data-ttu-id="b2d3f-163">Использование поставщика OpenSearch</span><span class="sxs-lookup"><span data-stu-id="b2d3f-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d3f-164">{Сеарчтермс}</span><span class="sxs-lookup"><span data-stu-id="b2d3f-164">{searchTerms}</span></span>    | <span data-ttu-id="b2d3f-165">Заменяются терминами поиска, которые пользователь вводит в поле ввода поиска проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="b2d3f-166">startIndex</span><span class="sxs-lookup"><span data-stu-id="b2d3f-166">{startIndex}</span></span>     | <span data-ttu-id="b2d3f-167">Используется при получении результатов в "Pages".</span><span class="sxs-lookup"><span data-stu-id="b2d3f-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="b2d3f-168">Заменяется индексом для первого возвращаемого элемента результата.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="b2d3f-169">StartPage</span><span class="sxs-lookup"><span data-stu-id="b2d3f-169">{startPage}</span></span>      | <span data-ttu-id="b2d3f-170">Используется при получении результатов в "Pages".</span><span class="sxs-lookup"><span data-stu-id="b2d3f-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="b2d3f-171">Заменяется номером страницы набора возвращаемых результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="b2d3f-172">расчета</span><span class="sxs-lookup"><span data-stu-id="b2d3f-172">{count}</span></span>          | <span data-ttu-id="b2d3f-173">Используется при получении результатов в "Pages".</span><span class="sxs-lookup"><span data-stu-id="b2d3f-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="b2d3f-174">Заменяется на число результатов поиска на каждой странице, запрашиваемых проводником Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="b2d3f-175">языке</span><span class="sxs-lookup"><span data-stu-id="b2d3f-175">{language}</span></span>       | <span data-ttu-id="b2d3f-176">Заменяется строкой, указывающей язык отправляемого запроса.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="b2d3f-177">{Инпутенкодинг}</span><span class="sxs-lookup"><span data-stu-id="b2d3f-177">{inputEncoding}</span></span>  | <span data-ttu-id="b2d3f-178">Заменяется строкой (например, UTF-16), которая указывает кодировку отправляемого запроса.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="b2d3f-179">OutputEncoding</span><span class="sxs-lookup"><span data-stu-id="b2d3f-179">{outputEncoding}</span></span> | <span data-ttu-id="b2d3f-180">Заменяется строкой (например, "UTF-16"), указывающей требуемую кодировку символов для ответа от веб-службы.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="b2d3f-181">Страничные результаты</span><span class="sxs-lookup"><span data-stu-id="b2d3f-181">Paged Results</span></span>

<span data-ttu-id="b2d3f-182">Может потребоваться ограничить количество возвращаемых результатов на запрос.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="b2d3f-183">Можно выбрать возврат "страницы" для получения результатов за раз или предоставить поставщику OpenSearch дополнительные страницы результатов по номеру элемента или номеру страницы.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="b2d3f-184">Например, при отправке двадцати результатов на страницу первая отправляемая страница начинается с индекса позиции 1 и на странице 1. Вторая отправляемая страница начинается с индекса позиции 21 и на странице 2.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="b2d3f-185">Вы можете определить, как поставщик OpenSearch должен запрашивать элементы, используя либо `{startItem}` `{startPage}` маркер в шаблоне URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="b2d3f-186">Разбиение на страницы с помощью индекса элемента</span><span class="sxs-lookup"><span data-stu-id="b2d3f-186">Paging Using the Item Index</span></span>

<span data-ttu-id="b2d3f-187">Индекс элемента определяет первый результирующий элемент на странице результатов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="b2d3f-188">Если требуется, чтобы клиенты отправляли запросы с помощью индекса элемента, можно использовать `{startIndex}` маркер в атрибуте **шаблона** элемента **URL** , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="b2d3f-189">Затем поставщик [OpenSearch](https://github.com/dewitt/opensearch) заменяет маркер в URL-адресе начальным значением индекса.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="b2d3f-190">Первый запрос начинается с первого элемента, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="b2d3f-191">Поставщик OpenSearch может получить дополнительные элементы, изменив `{startIndex}` значение параметра и выполнив новый запрос.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="b2d3f-192">Поставщик повторяет этот процесс до тех пор, пока не получит достаточное количество результатов, чтобы удовлетворить его предел, или достигнут конец результатов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="b2d3f-193">Поставщик OpenSearch проверяет количество элементов, возвращаемых веб-службой, на первой странице результатов и устанавливает для ожидаемого размера страницы это число.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="b2d3f-194">Он использует это число, чтобы увеличить `{startIndex}` значение для последующих запросов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="b2d3f-195">Например, если веб-служба возвращает 20 результатов в первом запросе, то поставщик устанавливает для ожидаемого размера страницы значение 20.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="b2d3f-196">Для следующего запроса поставщик заменяет `{startIndex}` значение 21, чтобы получить следующие 20 элементов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="b2d3f-197">Если страница результатов, возвращенная веб-службой, содержит меньше элементов, чем ожидалось, то поставщик OpenSearch считает, что он получил последнюю страницу результатов и прекращает выполнение запросов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="b2d3f-198">Разбиение на страницы с помощью индекса страниц</span><span class="sxs-lookup"><span data-stu-id="b2d3f-198">Paging Using the Page Index</span></span>

<span data-ttu-id="b2d3f-199">Индекс страницы определяет указанную страницу результатов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="b2d3f-200">Если требуется, чтобы клиенты отправляли запросы с помощью номера страницы, можно использовать `{startPage}` маркер в атрибуте **шаблона** элемента **URL-адреса** , чтобы указать, что, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="b2d3f-201">Затем поставщик OpenSearch заменяет маркер в URL-адресе параметром номера страницы.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="b2d3f-202">Первый запрос начинается с первой страницы, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="b2d3f-203">Если страница результатов, возвращенная веб-службой, содержит меньше элементов, чем ожидалось, то поставщик OpenSearch считает, что он получил последнюю страницу результатов и прекращает выполнение запросов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="b2d3f-204">Page Size</span><span class="sxs-lookup"><span data-stu-id="b2d3f-204">Page Size</span></span>

<span data-ttu-id="b2d3f-205">Может потребоваться настроить веб-службу, чтобы позволить запросу указывать размер страниц с помощью некоторого параметра в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="b2d3f-206">Запрос должен быть указан в OSDX--файле с помощью `{count}` токена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="b2d3f-207">Поставщик [OpenSearch](https://github.com/dewitt/opensearch) может установить требуемый размер страницы в количестве результатов на страницу, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="b2d3f-208">По умолчанию поставщик OpenSearch выполняет запросы, используя размер страницы 50.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="b2d3f-209">Если требуется другой размер страницы, не выведите `{count}` маркер и вместо этого поместите требуемое число непосредственно в элемент **шаблона URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="b2d3f-210">Поставщик OpenSearch определяет размер страницы на основе числа результатов, возвращенных при первом запросе.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="b2d3f-211">Если первая страница полученных результатов содержит меньше элементов, чем запрошенное количество, поставщик сбрасывает размер страницы для всех последующих запросов страницы.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="b2d3f-212">Если последующие запросы страницы возвращают меньшее количество элементов, чем было запрошено, поставщик OpenSearch предполагает, что достигнут конец результатов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="b2d3f-213">Расширенные элементы в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="b2d3f-214">Помимо стандартных элементов, федеративный поиск поддерживает следующие расширенные элементы: **максимумресулткаунт** и **ресултспроцессинг**.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="b2d3f-215">Поскольку эти расширенные дочерние элементы не поддерживаются в спецификации [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, их необходимо добавить с помощью следующего пространства имен:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="b2d3f-216">Максимальное число результатов</span><span class="sxs-lookup"><span data-stu-id="b2d3f-216">Maximum Result Count</span></span>

<span data-ttu-id="b2d3f-217">По умолчанию поисковые соединители ограничены 100 результатами на запрос пользователя.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="b2d3f-218">Это ограничение можно настроить, включив элемент **максимумресулткаунт** в файл OSD, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="b2d3f-219">В предыдущем примере префикс пространства имен объявляется `ms-ose` в элементе **опенсеарчдескриптион** верхнего уровня, а затем используется в качестве префикса в имени элемента.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="b2d3f-220">Это объявление является обязательным, так как **максимумресулткаунт** не поддерживается в спецификации [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="b2d3f-221">Сопоставление свойств</span><span class="sxs-lookup"><span data-stu-id="b2d3f-221">Property Mapping</span></span>

<span data-ttu-id="b2d3f-222">Когда веб-служба возвращает результаты в виде канала RSS или Atom, поставщик OpenSearch должен сопоставлять метаданные элементов в веб-каналах со свойствами, которые может использовать оболочка Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="b2d3f-223">На следующем снимке экрана показано, как поставщик OpenSearch сопоставляет некоторые из элементов RSS по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![снимок экрана с встроенными сопоставлениями свойств RSS-to-Windows-Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="b2d3f-225">Сопоставления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b2d3f-225">Default Mappings</span></span>

<span data-ttu-id="b2d3f-226">По умолчанию сопоставления XML-элементов RSS с системными свойствами оболочки Windows перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="b2d3f-227">Пути XML задаются относительно элемента Item.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="b2d3f-228">`"media:"`Префикс определяется пространством имен [поиска Yahoo](https://www.rssboard.org/media-rss) .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="b2d3f-229">XML-путь RSS</span><span class="sxs-lookup"><span data-stu-id="b2d3f-229">RSS XML path</span></span>                  | <span data-ttu-id="b2d3f-230">Свойство оболочки Windows (каноническое имя)</span><span class="sxs-lookup"><span data-stu-id="b2d3f-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="b2d3f-231">Ссылка</span><span class="sxs-lookup"><span data-stu-id="b2d3f-231">Link</span></span>                          | <span data-ttu-id="b2d3f-232">System. Итемурл</span><span class="sxs-lookup"><span data-stu-id="b2d3f-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="b2d3f-233">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2d3f-233">Title</span></span>                         | <span data-ttu-id="b2d3f-234">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="b2d3f-234">System.ItemName</span></span>                         |
| <span data-ttu-id="b2d3f-235">Автор</span><span class="sxs-lookup"><span data-stu-id="b2d3f-235">Author</span></span>                        | <span data-ttu-id="b2d3f-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="b2d3f-236">System.Author</span></span>                           |
| <span data-ttu-id="b2d3f-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="b2d3f-237">pubDate</span></span>                       | <span data-ttu-id="b2d3f-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="b2d3f-238">System.DateModified</span></span>                     |
| <span data-ttu-id="b2d3f-239">Описание</span><span class="sxs-lookup"><span data-stu-id="b2d3f-239">Description</span></span>                   | <span data-ttu-id="b2d3f-240">System. автосводка</span><span class="sxs-lookup"><span data-stu-id="b2d3f-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="b2d3f-241">Категория</span><span class="sxs-lookup"><span data-stu-id="b2d3f-241">Category</span></span>                      | <span data-ttu-id="b2d3f-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="b2d3f-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="b2d3f-243">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="b2d3f-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="b2d3f-244">System. size</span><span class="sxs-lookup"><span data-stu-id="b2d3f-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="b2d3f-245">System. Контентурл</span><span class="sxs-lookup"><span data-stu-id="b2d3f-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="b2d3f-246">носитель: Категория</span><span class="sxs-lookup"><span data-stu-id="b2d3f-246">media:category</span></span>                | <span data-ttu-id="b2d3f-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="b2d3f-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="b2d3f-248">System. size</span><span class="sxs-lookup"><span data-stu-id="b2d3f-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="b2d3f-249">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="b2d3f-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="b2d3f-250">System. Контентурл</span><span class="sxs-lookup"><span data-stu-id="b2d3f-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="b2d3f-251">System. size</span><span class="sxs-lookup"><span data-stu-id="b2d3f-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="b2d3f-252">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="b2d3f-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="b2d3f-253">System. Контентурл</span><span class="sxs-lookup"><span data-stu-id="b2d3f-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="b2d3f-254">System. Итемсумбнаилурл</span><span class="sxs-lookup"><span data-stu-id="b2d3f-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="b2d3f-255">Помимо сопоставления по умолчанию стандартных элементов RSS или Atom, можно сопоставить другие системные свойства оболочки Windows, включив дополнительные XML-элементы в пространство имен Windows для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="b2d3f-256">Можно также сопоставлять элементы из других существующих пространств имен XML, таких как Медиарсс, iTunes и т. д., путем добавления пользовательского сопоставления свойств в OSDX--файл.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="b2d3f-257">Сопоставления пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="b2d3f-257">Custom Property Mappings</span></span>

<span data-ttu-id="b2d3f-258">Вы можете настроить сопоставление элементов из выходных данных RSS с системными свойствами оболочки Windows, указав сопоставление в OSDX--файле.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="b2d3f-259">В выходных данных RSS указывается:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="b2d3f-260">Пространство имен XML и</span><span class="sxs-lookup"><span data-stu-id="b2d3f-260">An XML namespace, and</span></span>
-   <span data-ttu-id="b2d3f-261">Для любого дочернего элемента элемента — имя элемента для сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="b2d3f-262">OSDX--файл определяет свойство оболочки Windows для каждого имени элемента в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="b2d3f-263">Сопоставления свойств, определенные в файле. OSDX-, переопределяют сопоставления по умолчанию, если они существуют, для указанных свойств.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="b2d3f-264">На следующей схеме показано, как расширение RSS сопоставляется со свойствами Windows (каноническое имя).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![Схема, показывающая, что сочетание пространства имен XML и пути XML создает каноническое имя](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="b2d3f-266">Пример отображения результатов в формате RSS и свойства OSD</span><span class="sxs-lookup"><span data-stu-id="b2d3f-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="b2d3f-267">Следующий пример выходных данных RSS идентифицирует `https://example.com/schema/2009` как пространство имен XML с префиксом "example".</span><span class="sxs-lookup"><span data-stu-id="b2d3f-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="b2d3f-268">Этот префикс должен отображаться еще раз перед элементом **электронной почты** .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="b2d3f-269">В следующем примере файла. OSDX-элемент **электронной почты** XML сопоставляется со свойством оболочки Windows [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="b2d3f-270">Некоторые свойства не могут быть сопоставлены, так как их значения либо переопределены позже, либо не являются изменяемыми.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="b2d3f-271">Например, невозможно сопоставить [System. итемфолдерпасдисплай](../properties/props-system-itempathdisplay.md) или [System. итемпасдисплайнарров](../properties/props-system-itempathdisplaynarrow.md) , так как они вычисляются по значению URL-адреса, указанного в элементах Link или enclosure.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="b2d3f-272">Эскизы</span><span class="sxs-lookup"><span data-stu-id="b2d3f-272">Thumbnails</span></span>

<span data-ttu-id="b2d3f-273">URL-адреса изображений можно предоставить для любого элемента с помощью элемента **Media: thumbnail URL = ""** .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="b2d3f-274">Идеальное разрешение составляет 150 x 150 пикселей.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="b2d3f-275">Поддерживаются максимальные эскизы 256 x 256 пикселей.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="b2d3f-276">Предоставление большего количества образов требует больше пропускной способности, что не дает пользователю никаких дополнительных преимуществ.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="b2d3f-277">Открыть контекстное меню расположения файлов</span><span class="sxs-lookup"><span data-stu-id="b2d3f-277">Open File Location Context Menu</span></span>

<span data-ttu-id="b2d3f-278">Windows предоставляет контекстное меню с именем **открыть расположение файлов** для результатов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="b2d3f-279">Если пользователь выбирает элемент из этого меню, открывается "родительский" URL-адрес для выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="b2d3f-280">Если это URL-адрес, например `https://...` , веб-браузер открывается и переходит по этому URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="b2d3f-281">Для каждого элемента веб-канал должен предоставить настраиваемый URL для того, чтобы в Windows открывался допустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="b2d3f-282">Это можно сделать, включив URL-адрес внутри элемента внутри XML элемента, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="b2d3f-283">Если это свойство не задано явно в XML-коде элемента, поставщик OpenSearch устанавливает его в качестве родительской папки для URL-адреса элемента.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="b2d3f-284">В приведенном выше примере поставщик OpenSearch будет использовать значение Link и установить для свойства оболочки Windows [System. итемфолдерпасдисплай](../properties/props-system-itemfolderpathdisplay.md) значение `"https://example.com/"` .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="b2d3f-285">Настройка представлений проводника Windows с помощью списков описания свойств</span><span class="sxs-lookup"><span data-stu-id="b2d3f-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="b2d3f-286">Некоторые макеты представления проводника Windows определяются списками описания свойств или проплистс.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="b2d3f-287">Проплист — это разделенный точками с запятой список свойств, таких как `"prop:System.ItemName; System.Author"` , который используется для управления отображением результатов в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="b2d3f-288">Области пользовательского интерфейса проводника Windows, которые можно настроить с помощью проплистс, показаны на следующем снимке экрана:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![снимок экрана, в котором показаны области пользовательского интерфейса проводника Windows, которые можно настроить с помощью проплистс](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="b2d3f-290">Каждая область проводника имеет связанный набор проплистс, которые сами указываются как свойства.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="b2d3f-291">Можно указать пользовательские проплистс для отдельных элементов в результирующих наборах или для всех элементов в наборе результатов.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="b2d3f-292">Область пользовательского интерфейса для настройки</span><span class="sxs-lookup"><span data-stu-id="b2d3f-292">UI Area to customize</span></span>               | <span data-ttu-id="b2d3f-293">Свойство оболочки Windows, которое реализует настройку</span><span class="sxs-lookup"><span data-stu-id="b2d3f-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="b2d3f-294">Режим просмотра содержимого (при поиске)</span><span class="sxs-lookup"><span data-stu-id="b2d3f-294">Content view mode (when searching)</span></span> | <span data-ttu-id="b2d3f-295">System. Проплист. Контентвиевмодефорсеарч</span><span class="sxs-lookup"><span data-stu-id="b2d3f-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="b2d3f-296">Режим просмотра содержимого (при просмотре)</span><span class="sxs-lookup"><span data-stu-id="b2d3f-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="b2d3f-297">System. Проплист. Контентвиевмодефорбровсе</span><span class="sxs-lookup"><span data-stu-id="b2d3f-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="b2d3f-298">Режим мозаичного представления</span><span class="sxs-lookup"><span data-stu-id="b2d3f-298">Tile view mode</span></span>                     | <span data-ttu-id="b2d3f-299">System. Проплист. Тилеинфо</span><span class="sxs-lookup"><span data-stu-id="b2d3f-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="b2d3f-300">Область сведений</span><span class="sxs-lookup"><span data-stu-id="b2d3f-300">Details pane</span></span>                       | <span data-ttu-id="b2d3f-301">System. Проплист. Превиевдетаилс</span><span class="sxs-lookup"><span data-stu-id="b2d3f-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="b2d3f-302">Подсказка (Подсказка при наведении элемента)</span><span class="sxs-lookup"><span data-stu-id="b2d3f-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="b2d3f-303">System. Проплист. всплывающая подсказка</span><span class="sxs-lookup"><span data-stu-id="b2d3f-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="b2d3f-304">**Чтобы указать уникальный проплист для отдельного элемента, сделайте следующее:**</span><span class="sxs-lookup"><span data-stu-id="b2d3f-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="b2d3f-305">В выходных данных RSS Добавьте настраиваемый элемент, представляющий проплист, который необходимо настроить.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="b2d3f-306">Например, в следующем примере задается список для области сведений:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="b2d3f-307">Чтобы применить свойство к каждому элементу в результатах поиска без изменения выходных данных RSS, укажите проплист в элементе **MS-OSE: пропертидефаултвалуес** в файле OSDX-, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="b2d3f-308">Макет свойств в режиме просмотра содержимого</span><span class="sxs-lookup"><span data-stu-id="b2d3f-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="b2d3f-309">Список свойств, указанных в свойствах **System. проплист. контентвиевмодефорсеарч** и **System. проплист. контентвиевмодефорбровсе** проплистс, определяет, что отображается в режиме просмотра содержимого.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="b2d3f-310">Дополнительные сведения о списках свойств см. в разделе [проплист](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="b2d3f-311">Свойства размещаются в соответствии с числами, указанными в следующем шаблоне макета:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![снимок экрана, показывающий шаблон макета по умолчанию в представлении содержимого](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="b2d3f-313">Если используется следующий список свойств,</span><span class="sxs-lookup"><span data-stu-id="b2d3f-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="b2d3f-314">Затем отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-314">Then we see the following display:</span></span>

![снимок экрана с примером макета свойства.](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="b2d3f-316">Для лучшей удобочитаемости свойства, отображаемые в крайнем правом столбце, должны иметь метку.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="b2d3f-317">Флаги списка свойств</span><span class="sxs-lookup"><span data-stu-id="b2d3f-317">Property List Flags</span></span>

<span data-ttu-id="b2d3f-318">Только один из флагов, определенных в документации проплистс, применяется к отображению элементов в макетах в режиме просмотра содержимого: ` "~"` .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="b2d3f-319">В предыдущих примерах в представлении проводника Windows отображаются метки некоторых свойств, например `Tags: animals; zoo; lion` .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="b2d3f-320">Это поведение по умолчанию при указании свойства в списке.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="b2d3f-321">Например, проплист, `"System.Author"` который отображается как `"Authors: value"` .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="b2d3f-322">Если необходимо скрыть метку свойства, поместите `"~"` перед именем свойства.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="b2d3f-323">Например, если проплист имеет `"~System.Size"` значение, свойство отображается в виде значения, без метки.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="b2d3f-324">Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="b2d3f-324">Previews</span></span>

<span data-ttu-id="b2d3f-325">Когда пользователь выбирает элемент результата в проводнике Windows, а панель предварительного просмотра открыта, содержимое элемента отображается предварительно.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="b2d3f-326">Содержимое, отображаемое в предварительной версии, задается URL-адресом, который определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="b2d3f-327">Если для элемента задано свойство оболочки Windows **System. вебпревиевурл** , используйте этот URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="b2d3f-328">Свойство должно быть предоставлено в RSS с помощью пространства имен оболочки Windows или явно сопоставлено в OSDX--файле.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="b2d3f-329">Если это не так, используйте вместо этого URL-адрес ссылки.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="b2d3f-330">Эта логика показана в следующей блок-схеме.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-330">The following flowchart shows this logic.</span></span>

![Блок-схема, показывающая, как проводник Windows выбирает URL, используемый для предварительных версий](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="b2d3f-332">Можно использовать другой URL-адрес для предварительного просмотра, чем для самого элемента.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="b2d3f-333">Это означает, что если указать разные URL-адреса для ссылки и вложение, то `media:content URL` проводник Windows использует URL-адрес ссылки для предварительного просмотра элемента, но использует другой URL-адрес для обнаружения типа файла, открытия, загрузки и т. д.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="b2d3f-334">Как проводник Windows определяет, какой URL-адрес следует использовать:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="b2d3f-335">Если указать сопоставление для [System. итемфолдерпасдисплай](../properties/props-system-itemfolderpathdisplay.md), проводник Windows использует этот URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="b2d3f-336">Если сопоставление не указано, проводник Windows определяет, различаются ли URL-адреса ссылок и вложений.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="b2d3f-337">Если это так, проводник Windows использует URL-адрес ссылки.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="b2d3f-338">Если URL-адреса одинаковы или если имеется только URL-адрес ссылки, проводник Windows анализирует ссылку, чтобы найти родительский контейнер, удалив имя файла из полного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="b2d3f-339">Если вы знаете, что синтаксический анализ URL-адреса приведет к невозможности ссылок для службы, необходимо предоставить явное сопоставление для свойства.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="b2d3f-340">Открыть пункт меню "расположение файла"</span><span class="sxs-lookup"><span data-stu-id="b2d3f-340">Open File Location Menu Item</span></span>

<span data-ttu-id="b2d3f-341">При щелчке элемента правой кнопкой мыши отображается команда меню **открыть расположение файла** .</span><span class="sxs-lookup"><span data-stu-id="b2d3f-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="b2d3f-342">Эта команда переводит пользователя в контейнер для или расположения этого элемента.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="b2d3f-343">Например, в поиске SharePoint при выборе этого параметра для файла в библиотеке документов открывается корневой каталог библиотеки документов в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="b2d3f-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="b2d3f-344">Когда пользователь нажимает кнопку **открыть расположение файла**, проводник Windows пытается найти родительский контейнер, используя логику, показанную в следующей блок-схеме:</span><span class="sxs-lookup"><span data-stu-id="b2d3f-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![Блок-схема, показывающая, как проводник Windows определяет родительский контейнер](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="b2d3f-346">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b2d3f-346">Additional Resources</span></span>

<span data-ttu-id="b2d3f-347">Дополнительные сведения о реализации Федерации поиска в удаленных хранилищах данных с помощью технологий OpenSearch в Windows 7 и более поздних версиях см. в разделе "дополнительные ресурсы" в [Федеративной функции поиска в Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2d3f-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2d3f-348">См. также</span><span class="sxs-lookup"><span data-stu-id="b2d3f-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2d3f-349">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="b2d3f-350">начало работы с федеративными поиском в Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="b2d3f-351">Подключение веб-службы в Федеративной службе поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="b2d3f-352">Включение хранилища данных в федеративный поиск Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="b2d3f-353">Следующие рекомендации по использованию федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="b2d3f-354">Развертывание соединителей поиска в федеративного поиска Windows</span><span class="sxs-lookup"><span data-stu-id="b2d3f-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
