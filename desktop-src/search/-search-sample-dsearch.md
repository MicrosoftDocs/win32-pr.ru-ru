---
description: В примере кода Дсеарч показано, как создать класс для статического консольного приложения, чтобы запросить Поиск Windows с помощью сборки Microsoft. Search. Interop для Исеарчкуерихелпер.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: дсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692195"
---
# <a name="dsearch"></a><span data-ttu-id="568c5-103">дсеарч</span><span class="sxs-lookup"><span data-stu-id="568c5-103">DSearch</span></span>

<span data-ttu-id="568c5-104">В примере кода Дсеарч показано, как создать класс для статического консольного приложения, чтобы запросить Поиск Windows с помощью сборки Microsoft. Search. Interop для [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="568c5-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="568c5-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="568c5-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="568c5-106">Требования</span><span class="sxs-lookup"><span data-stu-id="568c5-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="568c5-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="568c5-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="568c5-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="568c5-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="568c5-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="568c5-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="568c5-110">См. также</span><span class="sxs-lookup"><span data-stu-id="568c5-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="568c5-111">Требования</span><span class="sxs-lookup"><span data-stu-id="568c5-111">Requirements</span></span>

| <span data-ttu-id="568c5-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="568c5-112">Product</span></span>     | <span data-ttu-id="568c5-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="568c5-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="568c5-114">Windows</span><span class="sxs-lookup"><span data-stu-id="568c5-114">Windows</span></span>     | <span data-ttu-id="568c5-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="568c5-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="568c5-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="568c5-116">Windows SDK</span></span> | <span data-ttu-id="568c5-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="568c5-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="568c5-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="568c5-118">Downloading the Sample</span></span>

<span data-ttu-id="568c5-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="568c5-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="568c5-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="568c5-120">Location</span></span>      | <span data-ttu-id="568c5-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="568c5-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="568c5-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="568c5-122">GitHub</span></span>        | [<span data-ttu-id="568c5-123">Пример Дсеарч</span><span class="sxs-lookup"><span data-stu-id="568c5-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="568c5-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="568c5-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="568c5-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="568c5-125">Building the Sample</span></span>

1. <span data-ttu-id="568c5-126">Откройте проводник Windows и перейдите в каталог проекта **дсеарч** .</span><span class="sxs-lookup"><span data-stu-id="568c5-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="568c5-127">Дважды щелкните значок файла Дсеарч. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="568c5-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="568c5-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="568c5-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="568c5-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="568c5-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="568c5-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="568c5-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="568c5-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="568c5-131">Running the Sample</span></span>

1. <span data-ttu-id="568c5-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="568c5-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="568c5-133">В командной строке введите `DSearch.exe` или в проводнике Windows дважды щелкните значок DSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="568c5-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="568c5-134">См. также</span><span class="sxs-lookup"><span data-stu-id="568c5-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="568c5-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="568c5-135">Reference</span></span>

[<span data-ttu-id="568c5-136">**исеарчкуерихелпер**</span><span class="sxs-lookup"><span data-stu-id="568c5-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="568c5-137">**исеарчкаталогманажер**</span><span class="sxs-lookup"><span data-stu-id="568c5-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="568c5-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="568c5-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="568c5-139">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="568c5-139">Other Samples</span></span>

[<span data-ttu-id="568c5-140">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="568c5-140">Search Code Samples</span></span>](-search-samples-ovw.md)
