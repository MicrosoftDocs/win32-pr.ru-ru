---
description: Узнайте, как Windows Search позволяет управлять индексом Windows Search с помощью диспетчера поиска, диспетчера каталогов и диспетчера области обхода содержимого.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Интерфейсы для управления индексом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120019"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="24e8c-103">Интерфейсы для управления индексом</span><span class="sxs-lookup"><span data-stu-id="24e8c-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="24e8c-104">Поиск Windows позволяет управлять индексом Windows Search с помощью трех основных компонентов: Диспетчер поиска, диспетчер каталогов и Диспетчер области обхода содержимого.</span><span class="sxs-lookup"><span data-stu-id="24e8c-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="24e8c-105">Некоторые из этих интерфейсов управления могут использоваться с правами обычного пользователя, но для тех, кто изменяет состояние индекса, требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="24e8c-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="24e8c-106">Сведения об интерфейсах для управления индексом</span><span class="sxs-lookup"><span data-stu-id="24e8c-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24e8c-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="24e8c-107">Component</span></span></th>
<th><span data-ttu-id="24e8c-108">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="24e8c-108">Interfaces</span></span></th>
<th><span data-ttu-id="24e8c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="24e8c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24e8c-110">Диспетчер поиска</span><span class="sxs-lookup"><span data-stu-id="24e8c-110">Search Manager</span></span></td>
<td><span data-ttu-id="24e8c-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">исеарчманажер</a></span><span class="sxs-lookup"><span data-stu-id="24e8c-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="24e8c-112">Предоставляет методы для получения и настройки сведений о поиске Windows:</span><span class="sxs-lookup"><span data-stu-id="24e8c-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="24e8c-113">Получение экземпляра диспетчера каталогов для определенного каталога.</span><span class="sxs-lookup"><span data-stu-id="24e8c-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="24e8c-114">Получение или Установка сведений о прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="24e8c-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="24e8c-115">Получение сведений о версии системы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="24e8c-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="24e8c-116">Дополнительные сведения см. <a href="-search-3x-wds-mngidx-searchmanager.md">в разделе Использование диспетчера поиска</a>.</span><span class="sxs-lookup"><span data-stu-id="24e8c-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24e8c-117">Диспетчер каталога</span><span class="sxs-lookup"><span data-stu-id="24e8c-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="24e8c-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">исеарчкаталогманажер</a></span><span class="sxs-lookup"><span data-stu-id="24e8c-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="24e8c-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="24e8c-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="24e8c-120">Предоставляет методы для управления отдельным каталогом поиска, например, что вызывает повторную индексацию или настройку времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="24e8c-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="24e8c-121">Этот интерфейс управляет каталогом в четырех областях:</span><span class="sxs-lookup"><span data-stu-id="24e8c-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="24e8c-122">Содержимое каталога — гарантируется, что новые данные индексируются и что другие приложения и компоненты работают надлежащим образом путем принудительной повторной индексации всего или части каталога или путем сброса всего каталога.</span><span class="sxs-lookup"><span data-stu-id="24e8c-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="24e8c-123">Свойства каталога — задание свойств, определяющих, как каталог управляет временем ожидания при подключении к обработчикам протоколов и как диакритические знаки обрабатываются при поиске.</span><span class="sxs-lookup"><span data-stu-id="24e8c-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="24e8c-124">Состояние каталога — получение сведений о каталоге, включая состояние, размер и текущее состояние действия.</span><span class="sxs-lookup"><span data-stu-id="24e8c-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="24e8c-125">Доступ к другим интерфейсам — получение других интерфейсов, связанных с поиском, требуемых диспетчером области сканирования, уведомлениями об изменении данных и интерфейсом <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>исеарчкуерихелпер</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24e8c-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="24e8c-126">Дополнительные сведения см. <a href="-search-3x-wds-mngidx-catalog-manager.md">в разделе Использование диспетчера каталогов</a>.</span><span class="sxs-lookup"><span data-stu-id="24e8c-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24e8c-127">Диспетчер области обхода содержимого</span><span class="sxs-lookup"><span data-stu-id="24e8c-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="24e8c-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>иенумсеарчрутс</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e8c-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="24e8c-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">иенумсеарчскоперулес</a></span><span class="sxs-lookup"><span data-stu-id="24e8c-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="24e8c-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>исеарчкравлскопеманажер</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e8c-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="24e8c-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="24e8c-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="24e8c-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>исеарчрут</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e8c-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="24e8c-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>исеарчскоперуле</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e8c-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="24e8c-134"><a href="/windows/desktop/search/-search-isearchitem">исеарчитем</a></span><span class="sxs-lookup"><span data-stu-id="24e8c-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="24e8c-135">Предоставляет методы для информирования поисковой системы о контейнерах для обхода или просмотра, а также элементов в этих контейнерах для включения или исключения в индексе.</span><span class="sxs-lookup"><span data-stu-id="24e8c-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="24e8c-136">Можно также запросить Диспетчер области сканирования, чтобы узнать, находится ли конкретный URL-адрес в области сканирования.</span><span class="sxs-lookup"><span data-stu-id="24e8c-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="24e8c-137">Дополнительные сведения см. <a href="-search-3x-wds-extidx-csm.md">в разделе Использование диспетчера области сканирования</a>.</span><span class="sxs-lookup"><span data-stu-id="24e8c-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="24e8c-138">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="24e8c-138">Related topics</span></span>

[<span data-ttu-id="24e8c-139">Управление индексом</span><span class="sxs-lookup"><span data-stu-id="24e8c-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="24e8c-140">Использование диспетчера поиска</span><span class="sxs-lookup"><span data-stu-id="24e8c-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="24e8c-141">Использование диспетчера каталогов</span><span class="sxs-lookup"><span data-stu-id="24e8c-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="24e8c-142">Использование диспетчера области сканирования</span><span class="sxs-lookup"><span data-stu-id="24e8c-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
