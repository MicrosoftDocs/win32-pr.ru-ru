---
description: В образце кода Кравлскопекоммандлине показано, как определить параметры командной строки для операций индексирования диспетчера области сканирования (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: кравлскопекоммандлине
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710919"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="030ec-103">кравлскопекоммандлине</span><span class="sxs-lookup"><span data-stu-id="030ec-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="030ec-104">В образце кода Кравлскопекоммандлине показано, как определить параметры командной строки для операций индексирования диспетчера области сканирования (CSM).</span><span class="sxs-lookup"><span data-stu-id="030ec-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="030ec-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="030ec-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="030ec-106">Требования</span><span class="sxs-lookup"><span data-stu-id="030ec-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="030ec-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="030ec-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="030ec-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="030ec-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="030ec-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="030ec-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="030ec-110">См. также</span><span class="sxs-lookup"><span data-stu-id="030ec-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="030ec-111">Требования</span><span class="sxs-lookup"><span data-stu-id="030ec-111">Requirements</span></span>

| <span data-ttu-id="030ec-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="030ec-112">Product</span></span>     | <span data-ttu-id="030ec-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="030ec-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="030ec-114">Windows</span><span class="sxs-lookup"><span data-stu-id="030ec-114">Windows</span></span>     | <span data-ttu-id="030ec-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="030ec-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="030ec-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="030ec-116">Windows SDK</span></span> | <span data-ttu-id="030ec-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="030ec-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="030ec-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="030ec-118">Downloading the Sample</span></span>

<span data-ttu-id="030ec-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="030ec-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="030ec-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="030ec-120">Location</span></span> | <span data-ttu-id="030ec-121">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="030ec-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="030ec-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="030ec-122">GitHub</span></span>   |    [<span data-ttu-id="030ec-123">Пример Кравлскопекоммандлине</span><span class="sxs-lookup"><span data-stu-id="030ec-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="030ec-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="030ec-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="030ec-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="030ec-125">Building the Sample</span></span>

1. <span data-ttu-id="030ec-126">Откройте проводник Windows и перейдите в каталог проекта **кравлскопекоммандлине** .</span><span class="sxs-lookup"><span data-stu-id="030ec-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="030ec-127">Дважды щелкните значок файла ксмкмд. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="030ec-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="030ec-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="030ec-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="030ec-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="030ec-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="030ec-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="030ec-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="030ec-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="030ec-131">Running the Sample</span></span>

1. <span data-ttu-id="030ec-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="030ec-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="030ec-133">В командной строке введите `csmcmd.exe` или в проводнике Windows дважды щелкните значок csmcmd.exe.</span><span class="sxs-lookup"><span data-stu-id="030ec-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="030ec-134">См. также</span><span class="sxs-lookup"><span data-stu-id="030ec-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="030ec-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="030ec-135">Reference</span></span>

[<span data-ttu-id="030ec-136">**иенумсеарчрутс**</span><span class="sxs-lookup"><span data-stu-id="030ec-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="030ec-137">**иенумсеарчскоперулес**</span><span class="sxs-lookup"><span data-stu-id="030ec-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="030ec-138">**исеарчкравлскопеманажер**</span><span class="sxs-lookup"><span data-stu-id="030ec-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="030ec-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="030ec-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="030ec-140">**исеарчрут**</span><span class="sxs-lookup"><span data-stu-id="030ec-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="030ec-141">**исеарчскоперуле**</span><span class="sxs-lookup"><span data-stu-id="030ec-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="030ec-142">**исеарчкаталогманажер**</span><span class="sxs-lookup"><span data-stu-id="030ec-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="030ec-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="030ec-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="030ec-144">**исеарчманажер**</span><span class="sxs-lookup"><span data-stu-id="030ec-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="030ec-145">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="030ec-145">Other Samples</span></span>

[<span data-ttu-id="030ec-146">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="030ec-146">Search Code Samples</span></span>](-search-samples-ovw.md)
