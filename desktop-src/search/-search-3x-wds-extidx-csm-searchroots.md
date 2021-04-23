---
description: Диспетчер области обхода содержимого (CSM) позволяет добавлять и удалять корни поиска для хранилищ данных в области сканирования Windows Search и из нее.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Управление корнями поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262946"
---
# <a name="managing-search-roots"></a><span data-ttu-id="2d867-103">Управление корнями поиска</span><span class="sxs-lookup"><span data-stu-id="2d867-103">Managing Search Roots</span></span>

<span data-ttu-id="2d867-104">Диспетчер области обхода содержимого (CSM) позволяет добавлять и удалять корни поиска для хранилищ данных в области сканирования Windows Search и из нее.</span><span class="sxs-lookup"><span data-stu-id="2d867-104">The Crawl Scope Manager (CSM) enables you to add and remove search roots for your data stores to and from the Windows Search crawl scope.</span></span>

<span data-ttu-id="2d867-105">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="2d867-105">This topic includes the following subjects:</span></span>

-   [<span data-ttu-id="2d867-106">Сведения об корнях поиска</span><span class="sxs-lookup"><span data-stu-id="2d867-106">About Search Roots</span></span>](#about-search-roots)
-   [<span data-ttu-id="2d867-107">Перед началом</span><span class="sxs-lookup"><span data-stu-id="2d867-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="2d867-108">Windows 7: новый API диспетчера области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="2d867-108">Windows 7: New Crawl Scope Manager API</span></span>](#windows-7-new-crawl-scope-manager-api)
-   [<span data-ttu-id="2d867-109">Добавление корней к области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="2d867-109">Adding Roots to the Crawl Scope</span></span>](#adding-roots-to-the-crawl-scope)
-   [<span data-ttu-id="2d867-110">Удаление корней из области сканирования</span><span class="sxs-lookup"><span data-stu-id="2d867-110">Removing Roots from the Crawl Scope</span></span>](#removing-roots-from-the-crawl-scope)
-   [<span data-ttu-id="2d867-111">Перечисление корней в области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="2d867-111">Enumerating Roots in the Crawl Scope</span></span>](#enumerating-roots-in-the-crawl-scope)
-   [<span data-ttu-id="2d867-112">См. также</span><span class="sxs-lookup"><span data-stu-id="2d867-112">Related topics</span></span>](#related-topics)

 

## <a name="about-search-roots"></a><span data-ttu-id="2d867-113">Сведения об корнях поиска</span><span class="sxs-lookup"><span data-stu-id="2d867-113">About Search Roots</span></span>

<span data-ttu-id="2d867-114">Корень поиска определяет основу пространства имен оболочки, в которой определенные области можно включать или исключать, и обычно является контейнером самого высокого уровня в протоколе, который можно перечислить.</span><span class="sxs-lookup"><span data-stu-id="2d867-114">A search root defines the base of a Shell namespace where specific scopes could be included or excluded, and is usually the highest level container in a protocol that can be enumerated.</span></span> <span data-ttu-id="2d867-115">Он не указывает, какие части этого хранилища должны быть проиндексированы или не должны индексироваться. Он просто сигнализирует, что хранилище содержимого существует и связано с зарегистрированным обработчиком протокола.</span><span class="sxs-lookup"><span data-stu-id="2d867-115">It does not specify which parts of this store should or should not be indexed; it merely signals that a content store exists and is associated with a registered protocol handler.</span></span> <span data-ttu-id="2d867-116">Синтаксис для идентификации корневого URL-адреса поиска включает протокол, идентификатор безопасности магазина или пользователя, путь и, при необходимости, конкретный элемент (например, файл).</span><span class="sxs-lookup"><span data-stu-id="2d867-116">The syntax for identifying a search root URL includes the protocol, the store or user's security identifier, the path, and optionally a specific item (like a file).</span></span> <span data-ttu-id="2d867-117">В следующих примерах показаны две формы синтаксиса для корня поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-117">The following examples show two forms of the syntax for a search root.</span></span>


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



<span data-ttu-id="2d867-118"><protocol>За сегментом должны следовать две (2) косые черты ("/"), если только это не файл: протокол, для которого требуется три косые черты (file:///).</span><span class="sxs-lookup"><span data-stu-id="2d867-118">The <protocol> segment must be followed by two (2) forward slashes ('/') unless it is the file: protocol, which requires three slashes (file:///).</span></span> <span data-ttu-id="2d867-119"><site or SID>Сегмент представляет хранилище содержимого или идентификатор безопасности пользователя, если корневой каталог поиска предназначен только для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d867-119">The <site or SID> segment represents either a content store or a user security identifier if the search root is meant to be specific to the user.</span></span> <span data-ttu-id="2d867-120"><path>Сегмент представляет собой набор контейнеров, таких как каталоги или папки, и может включать символ-шаблон " \* ".</span><span class="sxs-lookup"><span data-stu-id="2d867-120">The <path> segment is a set of containers, like directories or folders, and can include the wildcard character '\*'.</span></span> <span data-ttu-id="2d867-121">Классу</span><span class="sxs-lookup"><span data-stu-id="2d867-121">The</span></span> <item> <span data-ttu-id="2d867-122">сегмент является необязательным и может включать символ-шаблон " \* ".</span><span class="sxs-lookup"><span data-stu-id="2d867-122">segment is optional and can also include the wildcard character '\*'.</span></span> <span data-ttu-id="2d867-123">Если элемент не включен, обязательно завершите сегмент пути косой чертой, иначе индексатор будет считать, что последний вложенный элемент является элементом.</span><span class="sxs-lookup"><span data-stu-id="2d867-123">If you do not include an item, be sure to finish your path segment with a slash or the indexer will assume that the last subcontainer is an item.</span></span>

<span data-ttu-id="2d867-124">Например, предположим, что вы реализовали обработчик протокола (миф) для обработки файлов типа \* . myext для пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="2d867-124">For example, suppose you have implemented a protocol handler (myPH) to handle files of type \*.myext for a custom application.</span></span> <span data-ttu-id="2d867-125">Все эти файлы будут расположены в папке Ворктеама \\ ProjectFiles на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2d867-125">All of these files will be located in the folder WorkteamA\\ProjectFiles on a local computer.</span></span> <span data-ttu-id="2d867-126">Корень поиска для этого может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d867-126">The search root for that might look like this:</span></span>

-   <span data-ttu-id="2d867-127">myPH:///C: \\ ворктеама \\ ProjectFiles</span><span class="sxs-lookup"><span data-stu-id="2d867-127">myPH:///C:\\WorkteamA\\ProjectFiles</span></span>\\

<span data-ttu-id="2d867-128">Предположим, вы планируете включить все файлы. myext, но в индексе нет ничего другого из этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="2d867-128">Suppose you are planning to include all .myext files but nothing else from that container in the index.</span></span> <span data-ttu-id="2d867-129">Корень поиска для этого может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d867-129">The search root for that might look like this:</span></span>

-   <span data-ttu-id="2d867-130">myPH:///C: \\ ворктеама \\ ProjectFiles \\ \* . myext.</span><span class="sxs-lookup"><span data-stu-id="2d867-130">myPH:///C:\\WorkteamA\\ProjectFiles\\\*.myext.</span></span>

<span data-ttu-id="2d867-131">Шаблоны с подстановочными знаками определяют URL-адреса с помощью подстановочного знака " \* " и считаются шаблоном, а не URL-адресом, но терминология часто взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="2d867-131">Wildcard patterns define URLs by using the wildcard character '\*' and are considered a pattern rather than a URL, but the terminology is often used interchangeably.</span></span> <span data-ttu-id="2d867-132">Например, file:///C: \\ данные Project a \\ \* \\ \\ будут соответствовать следующим URL-адресам:</span><span class="sxs-lookup"><span data-stu-id="2d867-132">For example, file:///C:\\ProjectA\\\*\\data\\ would match the following URLs:</span></span>

-   <span data-ttu-id="2d867-133">В. \\ проектная \\ **версии 1** \\ данных</span><span class="sxs-lookup"><span data-stu-id="2d867-133">C:\\ProjectA\\**version1**\\data</span></span>\\
-   <span data-ttu-id="2d867-134">В. \\ проектная \\ **версия2** \\ данных</span><span class="sxs-lookup"><span data-stu-id="2d867-134">C:\\ProjectA\\**version2**\\data</span></span>\\

<span data-ttu-id="2d867-135">Но этот шаблон не будет соответствовать этому URL-адресу:</span><span class="sxs-lookup"><span data-stu-id="2d867-135">But that pattern would not match this URL:</span></span>

-   <span data-ttu-id="2d867-136">В. \\ проект a \\ **версии 1 \\ временные** \\ данные</span><span class="sxs-lookup"><span data-stu-id="2d867-136">C:\\ProjectA\\**version1\\temp**\\data</span></span>\\

<span data-ttu-id="2d867-137">Необходимо создать новые корни поиска для контейнеров, которые еще не находятся в области обхода содержимого индексатора.</span><span class="sxs-lookup"><span data-stu-id="2d867-137">You should create new search roots for containers that are not already in the crawl scope of the indexer.</span></span> <span data-ttu-id="2d867-138">Если путь C: \\ парентскопе уже включен в область сканирования, нет необходимости добавлять новый корневой элемент поиска для C: \\ парентскопе \\ чилдскопе, если не известно, что дочерняя область ранее не была исключена.</span><span class="sxs-lookup"><span data-stu-id="2d867-138">If path C:\\ParentScope is already included in the crawl scope, you do not need to add a new search root for C:\\ParentScope\\ChildScope unless you know that the child scope was previously excluded.</span></span>

<span data-ttu-id="2d867-139">Пользовательский интерфейс для настройки параметров поиска Windows отображает корни поиска для пользователей, чтобы они могли уточнить правила области для их поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-139">The user interface for setting Windows Search options displays search roots to users so they can refine the scope rules for their searches.</span></span> <span data-ttu-id="2d867-140">В рамках процесса установки пользовательского обработчика протокола, контейнера или приложения можно определить область обхода по умолчанию с правилами включения и исключения.</span><span class="sxs-lookup"><span data-stu-id="2d867-140">As part of the installation process for your custom protocol handler, container, and/or application, you might define a default crawl scope, with inclusion and exclusion rules.</span></span> <span data-ttu-id="2d867-141">Эти правила представлены для конечных пользователей в качестве расположений.</span><span class="sxs-lookup"><span data-stu-id="2d867-141">These rules are presented to end users as locations.</span></span> <span data-ttu-id="2d867-142">Пользователи могут перемещаться по подкаталогам предопределенного корня поиска и выбирать те из них, которые необходимо включить в поиск, или очистить те, которые нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="2d867-142">Users can navigate within the subdirectories of your predefined search root and select the ones they want to include in searches or clear the ones they want to exclude.</span></span>

 

## <a name="before-you-begin"></a><span data-ttu-id="2d867-143">Перед началом</span><span class="sxs-lookup"><span data-stu-id="2d867-143">Before You Begin</span></span>

<span data-ttu-id="2d867-144">Прежде чем использовать интерфейсы диспетчера области сканирования (CSM), необходимо выполнить следующие предварительные действия.</span><span class="sxs-lookup"><span data-stu-id="2d867-144">Before you can use any of the Crawl Scope Manager (CSM) interfaces, you must perform the following prerequisite steps:</span></span>

1.  <span data-ttu-id="2d867-145">Создайте объект **кравлсеарчманажер** и получите его интерфейс [**исеарчманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="2d867-145">Create the **CrawlSearchManager** object and obtain its [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) interface.</span></span>
2.  <span data-ttu-id="2d867-146">Вызовите [**исеарчманажер:: catalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) для "системиндекс", чтобы получить экземпляр интерфейса [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="2d867-146">Call [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) for "SystemIndex" to obtain an instance of an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface.</span></span>
3.  <span data-ttu-id="2d867-147">Вызовите метод [**исеарчкаталогманажер:: жеткравлскопеманажер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) , чтобы получить экземпляр интерфейса [**исеарчкравлскопеманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .</span><span class="sxs-lookup"><span data-stu-id="2d867-147">Call [**ISearchCatalogManager::GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) to obtain an instance of [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.</span></span>

<span data-ttu-id="2d867-148">После внесения изменений в Диспетчер области обхода содержимого (CSM) необходимо вызвать [**исеарчкравлскопеманажер:: савеалл**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall).</span><span class="sxs-lookup"><span data-stu-id="2d867-148">After making any changes to the Crawl Scope Manager (CSM), you must call [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall).</span></span> <span data-ttu-id="2d867-149">Этот метод не принимает параметров и возвращает значение S \_ ОК в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="2d867-149">This method takes no parameters and returns S\_OK on success.</span></span>

 

## <a name="windows-7-new-crawl-scope-manager-api"></a><span data-ttu-id="2d867-150">Windows 7: новый API диспетчера области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="2d867-150">Windows 7: New Crawl Scope Manager API</span></span>

<span data-ttu-id="2d867-151">В **Windows 7 и более поздних версиях** [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) расширяет функциональные возможности интерфейса [**исеарчкравлскопеманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .</span><span class="sxs-lookup"><span data-stu-id="2d867-151">In **Windows 7 and later**, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends the functionality of the [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.</span></span> <span data-ttu-id="2d867-152">Метод [**ISearchCrawlScopeManager2::-Version**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) получает версию диспетчера области СКАНИРОВАНИЯ (CSM), которая информирует клиентов, если изменилось состояние CSM.</span><span class="sxs-lookup"><span data-stu-id="2d867-152">The [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method gets the Crawl Scope Manager (CSM) version, which informs clients if the state of the CSM has changed.</span></span> <span data-ttu-id="2d867-153">**ISearchCrawlScopeManager2::-Version** не приводит к вызову между процессами.</span><span class="sxs-lookup"><span data-stu-id="2d867-153">**ISearchCrawlScopeManager2::GetVersion** does not result in a cross-process call.</span></span> <span data-ttu-id="2d867-154">Если функция выполнена, возвращаемый указатель остается действительным до тех пор, пока клиент не вызовет **UnmapViewOfFile** в указателе и **CloseHandle** на возвращенном обработчике.</span><span class="sxs-lookup"><span data-stu-id="2d867-154">If the function succeeds, then the pointer that is returned remains valid until the client calls **UnmapViewOfFile** on the pointer and **CloseHandle** on the returned handle.</span></span>

 

## <a name="adding-roots-to-the-crawl-scope"></a><span data-ttu-id="2d867-155">Добавление корней к области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="2d867-155">Adding Roots to the Crawl Scope</span></span>

<span data-ttu-id="2d867-156">[**Исеарчкравлскопеманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) сообщает поисковой системе о контейнерах для обхода и (или) просмотра, а также элементов в этих контейнерах для включения или исключения.</span><span class="sxs-lookup"><span data-stu-id="2d867-156">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) tells the search engine about containers to crawl and/or watch, and items under those containers to include or exclude.</span></span> <span data-ttu-id="2d867-157">Чтобы добавить новый корень поиска, создайте экземпляр объекта [**исеарчрут**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) , установите корневые атрибуты, а затем вызовите [**Исеарчкравлскопеманажер:: аддрут**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) и передайте ему указатель на объект **исеарчрут** .</span><span class="sxs-lookup"><span data-stu-id="2d867-157">To add a new search root, instantiate an [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) object, set the root attributes, and then call [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) and pass it a pointer to your **ISearchRoot** object.</span></span> <span data-ttu-id="2d867-158">Корневой URL-адрес поиска имеет ту же форму, что и корень поиска, описанный выше.</span><span class="sxs-lookup"><span data-stu-id="2d867-158">The search root URL takes the same form as the search root described earlier.</span></span>

<span data-ttu-id="2d867-159">В следующей таблице описаны соответствующие методы размещения для [**исеарчрут**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot). в настоящее время Поиск Windows не использует другие методы размещения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2d867-159">The following table describes the relevant put methods for [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); the interface's other put methods are not used currently by Windows Search.</span></span> <span data-ttu-id="2d867-160">Мы рекомендуем включить идентификаторы безопасности (SID) пользователей во всех корнях для повышения безопасности.</span><span class="sxs-lookup"><span data-stu-id="2d867-160">We recommend including the users' security identifiers (SIDs) in all roots for better security.</span></span> <span data-ttu-id="2d867-161">Корни на пользователя более безопасны, так как запросы выполняются в пользовательском процессе, что гарантирует, что один пользователь не сможет видеть элементы, индексируемые из папки "Входящие" другого пользователя, например.</span><span class="sxs-lookup"><span data-stu-id="2d867-161">Per-user roots are more secure as queries are run in a per-user process, ensuring that one user cannot see items indexed from another user's inbox, for example.</span></span>



| <span data-ttu-id="2d867-162">Метод</span><span class="sxs-lookup"><span data-stu-id="2d867-162">Method</span></span>                     | <span data-ttu-id="2d867-163">Описание</span><span class="sxs-lookup"><span data-stu-id="2d867-163">Description</span></span>                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d867-164">разместить \_ провидеснотификатионс</span><span class="sxs-lookup"><span data-stu-id="2d867-164">put\_ProvidesNotifications</span></span> | <span data-ttu-id="2d867-165">Задайте значение **true** , если обработчик протокола или другое приложение уведомит поисковую подсистему об изменениях в URL-адресах в корне поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-165">Set to **TRUE** if a protocol handler or other application will notify the search engine about changes to the URLs under the search root.</span></span> <span data-ttu-id="2d867-166">Уведомление указывает, что URL-адреса требуют повторного индексирования.</span><span class="sxs-lookup"><span data-stu-id="2d867-166">The notification indicates that the URLs need reindexing.</span></span> |
| <span data-ttu-id="2d867-167">разместить \_ рутурл</span><span class="sxs-lookup"><span data-stu-id="2d867-167">put\_RootURL</span></span>               | <span data-ttu-id="2d867-168">Задает корневой URL-адрес для текущего поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-168">Sets the root URL of the current search.</span></span> <span data-ttu-id="2d867-169">URL-адрес принимает описанную выше корневую форму поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-169">The URL takes the search root form described earlier.</span></span>                                                                                                      |



 

 

<span data-ttu-id="2d867-170">По умолчанию индексатор не выполняет обход области при добавлении корня поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-170">By default, the indexer does not crawl a scope when you add a search root.</span></span> <span data-ttu-id="2d867-171">Необходимо также добавить правило включения для корня.</span><span class="sxs-lookup"><span data-stu-id="2d867-171">You must also add an include rule for the root.</span></span> <span data-ttu-id="2d867-172">Если вы хотите добавить пользовательский корневой элемент для приложения, это приложение должно добавить соответствующие корни для новых пользователей при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="2d867-172">If you want to add a user-specific root for an application, that application should add the appropriate roots for new users when the application starts.</span></span>

<span data-ttu-id="2d867-173">Чтобы добавить соответствующие корни для новых пользователей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d867-173">To add the appropriate roots for new users:</span></span>

1.  <span data-ttu-id="2d867-174">Получите идентификатор безопасности пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d867-174">Get the user's SID.</span></span>
2.  <span data-ttu-id="2d867-175">Перечислите все корни, чтобы проверить, существует ли для этого идентификатора безопасности один из них.</span><span class="sxs-lookup"><span data-stu-id="2d867-175">Enumerate all roots to check whether one exists for this SID.</span></span>
3.  <span data-ttu-id="2d867-176">При необходимости добавьте новый корень с использованием идентификатора безопасности.</span><span class="sxs-lookup"><span data-stu-id="2d867-176">Add a new root, using the SID, if necessary.</span></span>

 

## <a name="removing-roots-from-the-crawl-scope"></a><span data-ttu-id="2d867-177">Удаление корней из области сканирования</span><span class="sxs-lookup"><span data-stu-id="2d867-177">Removing Roots from the Crawl Scope</span></span>

<span data-ttu-id="2d867-178">[**Исеарчкравлскопеманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) можно использовать для удаления корня из области сканирования, если больше не требуется индексировать этот URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2d867-178">You can use [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) to remove a root from the crawl scope when you no longer want that URL indexed.</span></span> <span data-ttu-id="2d867-179">При удалении корня также удаляются все правила области для этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2d867-179">Removing a root also deletes all scope rules for that URL.</span></span> <span data-ttu-id="2d867-180">Например, предположим, что требуется удалить хранилище содержимого и (или) его обработчик протокола из системы.</span><span class="sxs-lookup"><span data-stu-id="2d867-180">For example, suppose you want to uninstall a content store and/or its protocol handler from a system.</span></span> <span data-ttu-id="2d867-181">Можно удалить приложение, удалить все данные, а затем удалить корень поиска из области обхода содержимого, и Диспетчер области обхода контента удалит корень и все правила области, связанные с корнем.</span><span class="sxs-lookup"><span data-stu-id="2d867-181">You can uninstall the application, remove all data, and then remove the search root from the crawl scope, and the Crawl Scope Manager will remove the root and all scope rules associated with the root.</span></span>

<span data-ttu-id="2d867-182">Чтобы удалить существующий корень поиска, вызовите [**исеарчкравлскопеманажер:: ремоверут**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) с корнем поиска, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="2d867-182">To remove an existing search root, call [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) with the search root you want to remove.</span></span> <span data-ttu-id="2d867-183">Корневой URL-адрес поиска имеет ту же форму, что и корень поиска, описанный выше.</span><span class="sxs-lookup"><span data-stu-id="2d867-183">The search root URL takes the same form as the search root described earlier.</span></span> <span data-ttu-id="2d867-184">Этот метод возвращает \_ значение false, если корневой каталог не найден, и код ошибки, если произошла ошибка при удалении найденного корня.</span><span class="sxs-lookup"><span data-stu-id="2d867-184">This method returns S\_FALSE if the root is not found and an error code if there was an error removing a root that was found.</span></span>

<span data-ttu-id="2d867-185">При удалении корня поиска также удаляется URL-адрес из пользовательского интерфейса для параметров поиска Windows, поэтому пользователи могут не иметь возможности повторно добавить этот контейнер или расположение с помощью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2d867-185">Removing a search root also removes the URL from the user interface for Windows Search options, so users may not be able to re-add that container or location using the user interface.</span></span> <span data-ttu-id="2d867-186">Кроме того, можно удалить все переопределения набора пользователей для корня поиска и вернуться к исходным правилам корня и области поиска.</span><span class="sxs-lookup"><span data-stu-id="2d867-186">It is also possible to remove all user-set overrides of a search root and revert to the original search root and scope rules.</span></span> <span data-ttu-id="2d867-187">Дополнительные сведения см. в разделе [Управление правилами области](-search-3x-wds-extidx-csm-scoperules.md).</span><span class="sxs-lookup"><span data-stu-id="2d867-187">For more information, see [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md).</span></span>

> [!Note]  
> <span data-ttu-id="2d867-188">В Windows Vista, если пользователи удаляются с помощью профилей пользователей на панели управления, CSM удаляет все правила и корни с идентификатором безопасности и удаляет их индексированные элементы из каталога.</span><span class="sxs-lookup"><span data-stu-id="2d867-188">On Windows Vista, if users are removed through User Profiles in Control Panel, CSM removes all rules and roots with their SID and removes their indexed items from the catalog.</span></span> <span data-ttu-id="2d867-189">В Windows XP необходимо вручную удалить корни и правила пользователей.</span><span class="sxs-lookup"><span data-stu-id="2d867-189">On Windows XP, you need to remove the users' roots and rules manually.</span></span>

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a><span data-ttu-id="2d867-190">Перечисление корней в области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="2d867-190">Enumerating Roots in the Crawl Scope</span></span>

<span data-ttu-id="2d867-191">CSM перечисляет корни поиска с помощью стандартного интерфейса перечислителя в стиле COM, [**иенумсеарчрутс**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots).</span><span class="sxs-lookup"><span data-stu-id="2d867-191">The CSM enumerates search roots using a standard COM-style enumerator interface, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots).</span></span> <span data-ttu-id="2d867-192">Этот интерфейс можно использовать для перечисления корней поиска в ряде целей.</span><span class="sxs-lookup"><span data-stu-id="2d867-192">You can use this interface to enumerate search roots for a number of purposes.</span></span> <span data-ttu-id="2d867-193">Например, может потребоваться отобразить всю область сканирования в пользовательском интерфейсе или определить, находится ли конкретный корень или дочерний элемент корневого элемента в области обхода.</span><span class="sxs-lookup"><span data-stu-id="2d867-193">For example, you might want to display the entire crawl scope in a user interface, or discover whether a particular root or the child of a root is already in the crawl scope.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2d867-194">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2d867-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2d867-195">**Reference**</span><span class="sxs-lookup"><span data-stu-id="2d867-195">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d867-196">**исеарчкравлскопеманажер**</span><span class="sxs-lookup"><span data-stu-id="2d867-196">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[<span data-ttu-id="2d867-197">**исеарчрут**</span><span class="sxs-lookup"><span data-stu-id="2d867-197">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[<span data-ttu-id="2d867-198">**иенумсеарчрутс**</span><span class="sxs-lookup"><span data-stu-id="2d867-198">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

<span data-ttu-id="2d867-199">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2d867-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2d867-200">Использование диспетчера области сканирования</span><span class="sxs-lookup"><span data-stu-id="2d867-200">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[<span data-ttu-id="2d867-201">Управление правилами области</span><span class="sxs-lookup"><span data-stu-id="2d867-201">Managing Scope Rules</span></span>](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



