---
description: В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search с помощью язык SQL (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: всскл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896929"
---
# <a name="wssql"></a><span data-ttu-id="f460f-103">всскл</span><span class="sxs-lookup"><span data-stu-id="f460f-103">WSSQL</span></span>

<span data-ttu-id="f460f-104">В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search с помощью язык SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="f460f-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="f460f-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="f460f-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="f460f-106">Требования</span><span class="sxs-lookup"><span data-stu-id="f460f-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="f460f-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="f460f-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="f460f-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="f460f-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="f460f-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="f460f-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="f460f-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f460f-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="f460f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f460f-111">Requirements</span></span>

| <span data-ttu-id="f460f-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="f460f-112">Product</span></span>     | <span data-ttu-id="f460f-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="f460f-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="f460f-114">Windows</span><span class="sxs-lookup"><span data-stu-id="f460f-114">Windows</span></span>     | <span data-ttu-id="f460f-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="f460f-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="f460f-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f460f-116">Windows SDK</span></span> | <span data-ttu-id="f460f-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="f460f-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="f460f-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="f460f-118">Downloading the Sample</span></span>

<span data-ttu-id="f460f-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="f460f-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="f460f-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="f460f-120">Location</span></span>      | <span data-ttu-id="f460f-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="f460f-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f460f-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="f460f-122">GitHub</span></span>        | [<span data-ttu-id="f460f-123">Пример ВССКЛ</span><span class="sxs-lookup"><span data-stu-id="f460f-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="f460f-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="f460f-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="f460f-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="f460f-125">Building the Sample</span></span>

1. <span data-ttu-id="f460f-126">Откройте проводник Windows и перейдите в каталог проекта **всскл** .</span><span class="sxs-lookup"><span data-stu-id="f460f-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="f460f-127">Дважды щелкните значок файла ВССКЛ. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f460f-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="f460f-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="f460f-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="f460f-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="f460f-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="f460f-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="f460f-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f460f-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="f460f-131">Running the Sample</span></span>

1. <span data-ttu-id="f460f-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="f460f-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="f460f-133">В командной строке введите `WSSQL.exe` или в проводнике Windows дважды щелкните значок WSSQL.exe.</span><span class="sxs-lookup"><span data-stu-id="f460f-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f460f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f460f-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="f460f-135">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="f460f-135">Conceptual</span></span>

[<span data-ttu-id="f460f-136">Использование синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="f460f-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="f460f-137">Общие сведения о языке запросов</span><span class="sxs-lookup"><span data-stu-id="f460f-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="f460f-138">Общие сведения о программировании OLE DB</span><span class="sxs-lookup"><span data-stu-id="f460f-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="f460f-139">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="f460f-139">Other Samples</span></span>

[<span data-ttu-id="f460f-140">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="f460f-140">Search Code Samples</span></span>](-search-samples-ovw.md)
