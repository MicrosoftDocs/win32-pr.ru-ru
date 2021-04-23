---
description: Представляет схему описания соединителя поиска, которая используется библиотеками проводника Windows и службами федеративного поиска.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Схема описания соединителя поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701377"
---
# <a name="search-connector-description-schema"></a><span data-ttu-id="afcc6-103">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="afcc6-103">Search Connector Description Schema</span></span>

<span data-ttu-id="afcc6-104">Представляет схему описания соединителя поиска, которая используется библиотеками проводника Windows и службами федеративного поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="afcc6-105">Схема определяет структуру и требования для файлов описания соединителя поиска ( \* . сеарчконнектор-MS) и **сеарчконнектордескриптионтипе** элементов в файлах описания библиотеки оболочки ( \* . Library-MS).</span><span class="sxs-lookup"><span data-stu-id="afcc6-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="afcc6-106">В этом разделе описывается схема, связанная с соединителями федеративного поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="afcc6-107">Дополнительные сведения о библиотеках и схеме описания библиотеки см. в разделе [Библиотека описание схемы](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="afcc6-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="afcc6-108">Этот раздел включает следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="afcc6-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="afcc6-109">Что такое соединители поиска?</span><span class="sxs-lookup"><span data-stu-id="afcc6-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="afcc6-110">Как работают файлы описания соединителя поиска?</span><span class="sxs-lookup"><span data-stu-id="afcc6-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="afcc6-111">Что такое схема описания соединителя поиска?</span><span class="sxs-lookup"><span data-stu-id="afcc6-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="afcc6-112">Каковы основные части схемы?</span><span class="sxs-lookup"><span data-stu-id="afcc6-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="afcc6-113">Примеры файлов описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="afcc6-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="afcc6-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="afcc6-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="afcc6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="afcc6-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="afcc6-116">Что такое соединители поиска?</span><span class="sxs-lookup"><span data-stu-id="afcc6-116">What Are Search Connectors?</span></span>

<span data-ttu-id="afcc6-117">Соединители поиска соединяют пользователей с данными, хранящимися в веб-службах или в расположениях удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="afcc6-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="afcc6-118">В Windows 7 пользователи могут устанавливать соединители поиска для таких расположений, как веб-службы, чтобы они могли выполнять поиск в этих расположениях непосредственно из проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="afcc6-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="afcc6-119">Соединители поиска — это файлы описания соединителя поиска ( \* . сеарчконнектор-MS), которые определяют способ подключения к, отправки запросов и получения результатов из расположения.</span><span class="sxs-lookup"><span data-stu-id="afcc6-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="afcc6-120">Помимо веб-служб, соединители поиска можно использовать для поиска областей локальных индексов, созданных обработчиками протоколов.</span><span class="sxs-lookup"><span data-stu-id="afcc6-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="afcc6-121">Например, пользователи могут искать электронное письмо по электронной почте с помощью обработчика протокола MAPI, используя соединитель поиска для этого хранилища электронной почты.</span><span class="sxs-lookup"><span data-stu-id="afcc6-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="afcc6-122">Как работают файлы описания соединителя поиска?</span><span class="sxs-lookup"><span data-stu-id="afcc6-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="afcc6-123">Когда файлы описания соединителя поиска устанавливаются в системах пользователей, пользователи могут открыть проводник Windows, щелкнуть соединитель поиска в области навигации и ввести поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="afcc6-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="afcc6-124">Проводник Windows отправляет запрос, используя сведения из файла описания соединителя поиска, такие как используемый поставщик и область поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="afcc6-125">Результаты возвращаются в виде элементов канала RSS или Atom и отображаются пользователям как обычные элементы оболочки.</span><span class="sxs-lookup"><span data-stu-id="afcc6-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="afcc6-126">Развертывание файла описания соединителя поиска зависит от типа расположения, поддерживаемого соединителем поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="afcc6-127">В файле конфигурации OpenSearch ( \* . OSDX-) для веб-службы</span><span class="sxs-lookup"><span data-stu-id="afcc6-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="afcc6-128">В рамках установки обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="afcc6-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="afcc6-129">При открытии файла OSDX-или установке обработчика протокола необходимо убедиться, что выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="afcc6-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="afcc6-130">Файл. сеарчконнектор-MS создается в папке пользователей " **Поиск Windows** " (% UserProfile%/сеарчес).</span><span class="sxs-lookup"><span data-stu-id="afcc6-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="afcc6-131">Ярлык для файла. сеарчконнектор-MS создается в папке " **Links** " пользователей (% UserProfile%/Линкс).</span><span class="sxs-lookup"><span data-stu-id="afcc6-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="afcc6-132">Что такое схема описания соединителя поиска?</span><span class="sxs-lookup"><span data-stu-id="afcc6-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="afcc6-133">Схема описания соединителя поиска — это схема XML, которая определяет структуру файлов описания соединителя поиска ( \* . сеарчконнектор-MS).</span><span class="sxs-lookup"><span data-stu-id="afcc6-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="afcc6-134">Каждый соединитель поиска должен иметь файл описания соединителя поиска, указывающий способ подключения к, отправки запросов и получения результатов из расположения.</span><span class="sxs-lookup"><span data-stu-id="afcc6-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="afcc6-135">Каковы основные части схемы?</span><span class="sxs-lookup"><span data-stu-id="afcc6-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="afcc6-136">В следующей таблице перечислены основные части схемы.</span><span class="sxs-lookup"><span data-stu-id="afcc6-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="afcc6-137">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="afcc6-137">Child elements</span></span>                                                                         | <span data-ttu-id="afcc6-138">Описание</span><span class="sxs-lookup"><span data-stu-id="afcc6-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afcc6-139">иссеарчонлитем</span><span class="sxs-lookup"><span data-stu-id="afcc6-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="afcc6-140">Определяет, поддерживаются ли в соединителе поиска расположения только для поиска или поиска и просмотра.</span><span class="sxs-lookup"><span data-stu-id="afcc6-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="afcc6-141">исдефаултсавелокатион</span><span class="sxs-lookup"><span data-stu-id="afcc6-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="afcc6-142">Только для использования в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="afcc6-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="afcc6-143">исдефаултноновнерсавелокатион</span><span class="sxs-lookup"><span data-stu-id="afcc6-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="afcc6-144">Только для использования в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="afcc6-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="afcc6-145">description</span><span class="sxs-lookup"><span data-stu-id="afcc6-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="afcc6-146">Описывает соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="afcc6-147">иконреференце</span><span class="sxs-lookup"><span data-stu-id="afcc6-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="afcc6-148">Определяет расположение пользовательского значка для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="afcc6-149">имажелинк</span><span class="sxs-lookup"><span data-stu-id="afcc6-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="afcc6-150">Определяет расположение пользовательского эскиза для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="afcc6-151">календаря</span><span class="sxs-lookup"><span data-stu-id="afcc6-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="afcc6-152">Определяет автора соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="afcc6-153">dateCreated</span><span class="sxs-lookup"><span data-stu-id="afcc6-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="afcc6-154">Определяет дату создания соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="afcc6-155">темплатеинфо</span><span class="sxs-lookup"><span data-stu-id="afcc6-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="afcc6-156">Указывает тип папки для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="afcc6-157">локатионпровидер</span><span class="sxs-lookup"><span data-stu-id="afcc6-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="afcc6-158">Указывает поставщика поиска для использования этим соединителем поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="afcc6-159">область</span><span class="sxs-lookup"><span data-stu-id="afcc6-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="afcc6-160">Задает расположения для включения в область поиска и исключения из нее.</span><span class="sxs-lookup"><span data-stu-id="afcc6-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="afcc6-161">пропертисторе</span><span class="sxs-lookup"><span data-stu-id="afcc6-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="afcc6-162">Указывает расположение [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) на основе XML для этого соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="afcc6-163">**Ипропертисторе** поддерживает открытые метаданные соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="afcc6-164">инклудеинстартменускопе</span><span class="sxs-lookup"><span data-stu-id="afcc6-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="afcc6-165">Указывает, следует ли включать расположение, представленное соединителем поиска, в область поиска меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="afcc6-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="afcc6-166">поддомен</span><span class="sxs-lookup"><span data-stu-id="afcc6-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="afcc6-167">Определяет домен верхнего уровня соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="afcc6-168">суппортсадванцедкуерисинтакс</span><span class="sxs-lookup"><span data-stu-id="afcc6-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="afcc6-169">Указывает, поддерживает ли соединитель поиска расширенный синтаксис запросов (АКС).</span><span class="sxs-lookup"><span data-stu-id="afcc6-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="afcc6-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afcc6-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="afcc6-171">Указывает, индексировано ли расположение, представленное соединителем поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="afcc6-172">Примеры файлов описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="afcc6-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="afcc6-173">Ниже приведен пример файла описания соединителя поиска для федеративной веб-службы поиска.</span><span class="sxs-lookup"><span data-stu-id="afcc6-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="afcc6-174">Ниже приведен пример файла описания соединителя поиска для обработчика протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="afcc6-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a><span data-ttu-id="afcc6-175">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="afcc6-175">Additional Resources</span></span>

-   <span data-ttu-id="afcc6-176">Дополнительные сведения о схеме описания библиотеки см. в разделе [Библиотека описание схемы](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="afcc6-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="afcc6-177">Дополнительные сведения об установке соединителя поиска см. в статье [федеративный поиск в Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="afcc6-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="afcc6-178">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="afcc6-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="afcc6-179">**Reference**</span><span class="sxs-lookup"><span data-stu-id="afcc6-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="afcc6-180">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="afcc6-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="afcc6-181">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="afcc6-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="afcc6-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="afcc6-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="afcc6-183">Центре загрузки Майкрософт</span><span class="sxs-lookup"><span data-stu-id="afcc6-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
