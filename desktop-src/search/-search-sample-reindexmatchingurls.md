---
description: 'В примере кода Реиндексматчингурлс показано, как предоставить три способа указания файлов для повторного индексирования: URL-адреса, соответствующие типу файла, типу MIME или указанному предложению WHERE.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: реиндексматчингурлс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497067"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="c92de-103">реиндексматчингурлс</span><span class="sxs-lookup"><span data-stu-id="c92de-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="c92de-104">В примере кода Реиндексматчингурлс показано, как предоставить три способа указания файлов для повторного индексирования: URL-адреса, соответствующие типу файла, типу MIME или указанному предложению WHERE.</span><span class="sxs-lookup"><span data-stu-id="c92de-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="c92de-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="c92de-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c92de-106">Требования</span><span class="sxs-lookup"><span data-stu-id="c92de-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="c92de-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="c92de-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="c92de-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="c92de-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="c92de-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="c92de-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c92de-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c92de-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c92de-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c92de-111">Requirements</span></span>

| <span data-ttu-id="c92de-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="c92de-112">Product</span></span>     | <span data-ttu-id="c92de-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="c92de-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="c92de-114">Windows</span><span class="sxs-lookup"><span data-stu-id="c92de-114">Windows</span></span>     | <span data-ttu-id="c92de-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="c92de-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="c92de-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c92de-116">Windows SDK</span></span> | <span data-ttu-id="c92de-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="c92de-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="c92de-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="c92de-118">Downloading the Sample</span></span>

<span data-ttu-id="c92de-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="c92de-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="c92de-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="c92de-120">Location</span></span>      | <span data-ttu-id="c92de-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="c92de-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="c92de-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="c92de-122">GitHub</span></span>  | [<span data-ttu-id="c92de-123">Пример Реиндексматчингурлс</span><span class="sxs-lookup"><span data-stu-id="c92de-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="c92de-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="c92de-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c92de-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="c92de-125">Building the Sample</span></span>

1. <span data-ttu-id="c92de-126">Откройте проводник Windows и перейдите в каталог проекта **реиндексматчингурлс** .</span><span class="sxs-lookup"><span data-stu-id="c92de-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="c92de-127">Например, полный путь установки по умолчанию — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .</span><span class="sxs-lookup"><span data-stu-id="c92de-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="c92de-128">Дважды щелкните значок для повторного индексирования файла. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c92de-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="c92de-129">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="c92de-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="c92de-130">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="c92de-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="c92de-131">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="c92de-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c92de-132">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="c92de-132">Running the Sample</span></span>

1. <span data-ttu-id="c92de-133">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="c92de-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="c92de-134">В командной строке введите `Reindex.exe` или в проводнике Windows дважды щелкните значок Reindex.exe.</span><span class="sxs-lookup"><span data-stu-id="c92de-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c92de-135">См. также</span><span class="sxs-lookup"><span data-stu-id="c92de-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="c92de-136">Справочник</span><span class="sxs-lookup"><span data-stu-id="c92de-136">Reference</span></span>

[<span data-ttu-id="c92de-137">**исеарчкаталогманажер**</span><span class="sxs-lookup"><span data-stu-id="c92de-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="c92de-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="c92de-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="c92de-139">**исеарчманажер**</span><span class="sxs-lookup"><span data-stu-id="c92de-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="c92de-140">**исеарчперсистентитемсчанжедсинк**</span><span class="sxs-lookup"><span data-stu-id="c92de-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="c92de-141">**исеарчвиевчанжедсинк**</span><span class="sxs-lookup"><span data-stu-id="c92de-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="c92de-142">**определение приоритетов \_ флагов**</span><span class="sxs-lookup"><span data-stu-id="c92de-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="c92de-143">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="c92de-143">Other Samples</span></span>

[<span data-ttu-id="c92de-144">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="c92de-144">Search Code Samples</span></span>](-search-samples-ovw.md)
