---
description: В примере кода Ифилтерсампле показано, как создать базовый класс IFilter для реализации интерфейса IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: ифилтерсампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692194"
---
# <a name="ifiltersample"></a><span data-ttu-id="c4489-103">ифилтерсампле</span><span class="sxs-lookup"><span data-stu-id="c4489-103">IFilterSample</span></span>

<span data-ttu-id="c4489-104">В примере кода Ифилтерсампле показано, как создать базовый класс IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="c4489-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="c4489-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="c4489-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c4489-106">Требования</span><span class="sxs-lookup"><span data-stu-id="c4489-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="c4489-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="c4489-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="c4489-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="c4489-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="c4489-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="c4489-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c4489-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c4489-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c4489-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c4489-111">Requirements</span></span>

| <span data-ttu-id="c4489-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="c4489-112">Product</span></span>     | <span data-ttu-id="c4489-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="c4489-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="c4489-114">Windows</span><span class="sxs-lookup"><span data-stu-id="c4489-114">Windows</span></span>     | <span data-ttu-id="c4489-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="c4489-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="c4489-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c4489-116">Windows SDK</span></span> | <span data-ttu-id="c4489-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="c4489-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="c4489-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="c4489-118">Downloading the Sample</span></span>

<span data-ttu-id="c4489-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="c4489-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="c4489-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="c4489-120">Location</span></span>      | <span data-ttu-id="c4489-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="c4489-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c4489-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="c4489-122">GitHub</span></span>        | [<span data-ttu-id="c4489-123">ифилтерсампле</span><span class="sxs-lookup"><span data-stu-id="c4489-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="c4489-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="c4489-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c4489-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="c4489-125">Building the Sample</span></span>

1. <span data-ttu-id="c4489-126">Откройте проводник Windows и перейдите в каталог проекта **филтербасе** .</span><span class="sxs-lookup"><span data-stu-id="c4489-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="c4489-127">Дважды щелкните значок файла Филтербасе. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c4489-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="c4489-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="c4489-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="c4489-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="c4489-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="c4489-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="c4489-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c4489-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="c4489-131">Running the Sample</span></span>

1. <span data-ttu-id="c4489-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="c4489-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="c4489-133">В командной строке введите `FilterBase.exe` или в проводнике Windows дважды щелкните значок FilterBase.exe.</span><span class="sxs-lookup"><span data-stu-id="c4489-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4489-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c4489-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="c4489-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="c4489-135">Reference</span></span>

[<span data-ttu-id="c4489-136">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="c4489-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="c4489-137">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="c4489-137">Conceptual</span></span>

[<span data-ttu-id="c4489-138">Разработка обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="c4489-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="c4489-139">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="c4489-139">Other Samples</span></span>

[<span data-ttu-id="c4489-140">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="c4489-140">Search Code Samples</span></span>](-search-samples-ovw.md)
