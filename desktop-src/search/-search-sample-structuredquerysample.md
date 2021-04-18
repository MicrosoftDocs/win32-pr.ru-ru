---
description: В примере кода Структуредкуерисампле показано, как считывать строки из консоли, анализировать их с помощью системной схемы и отображать результирующие деревья условий.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: структуредкуерисампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692191"
---
# <a name="structuredquerysample"></a><span data-ttu-id="290fa-103">структуредкуерисампле</span><span class="sxs-lookup"><span data-stu-id="290fa-103">StructuredQuerySample</span></span>

<span data-ttu-id="290fa-104">В примере кода Структуредкуерисампле показано, как считывать строки из консоли, анализировать их с помощью системной схемы и отображать результирующие деревья условий.</span><span class="sxs-lookup"><span data-stu-id="290fa-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="290fa-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="290fa-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="290fa-106">Требования</span><span class="sxs-lookup"><span data-stu-id="290fa-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="290fa-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="290fa-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="290fa-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="290fa-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="290fa-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="290fa-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="290fa-110">См. также</span><span class="sxs-lookup"><span data-stu-id="290fa-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="290fa-111">Требования</span><span class="sxs-lookup"><span data-stu-id="290fa-111">Requirements</span></span>

| <span data-ttu-id="290fa-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="290fa-112">Product</span></span>     | <span data-ttu-id="290fa-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="290fa-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="290fa-114">Windows</span><span class="sxs-lookup"><span data-stu-id="290fa-114">Windows</span></span>     | <span data-ttu-id="290fa-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="290fa-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="290fa-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="290fa-116">Windows SDK</span></span> | <span data-ttu-id="290fa-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="290fa-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="290fa-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="290fa-118">Downloading the Sample</span></span>

<span data-ttu-id="290fa-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="290fa-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="290fa-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="290fa-120">Location</span></span>      | <span data-ttu-id="290fa-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="290fa-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="290fa-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="290fa-122">GitHub</span></span>        | [<span data-ttu-id="290fa-123">структуредкуерисампле</span><span class="sxs-lookup"><span data-stu-id="290fa-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="290fa-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="290fa-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="290fa-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="290fa-125">Building the Sample</span></span>

1. <span data-ttu-id="290fa-126">Откройте проводник Windows и перейдите в каталог проекта **структуредкуерисампле** .</span><span class="sxs-lookup"><span data-stu-id="290fa-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="290fa-127">Дважды щелкните значок файла Структуредкуерисампле. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="290fa-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="290fa-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="290fa-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="290fa-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="290fa-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="290fa-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="290fa-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="290fa-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="290fa-131">Running the Sample</span></span>

1. <span data-ttu-id="290fa-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="290fa-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="290fa-133">В командной строке введите `StructuredQuerySample.exe` или в проводнике Windows дважды щелкните значок StructuredQuerySample.exe.</span><span class="sxs-lookup"><span data-stu-id="290fa-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="290fa-134">См. также</span><span class="sxs-lookup"><span data-stu-id="290fa-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="290fa-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="290fa-135">Reference</span></span>

[<span data-ttu-id="290fa-136">**икондитион**</span><span class="sxs-lookup"><span data-stu-id="290fa-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="290fa-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="290fa-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="290fa-138">**икондитионфактори**</span><span class="sxs-lookup"><span data-stu-id="290fa-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="290fa-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="290fa-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="290fa-140">**икондитионженератор**</span><span class="sxs-lookup"><span data-stu-id="290fa-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="290fa-141">**икуерипарсер**</span><span class="sxs-lookup"><span data-stu-id="290fa-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="290fa-142">**икуерипарсерманажер**</span><span class="sxs-lookup"><span data-stu-id="290fa-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="290fa-143">**икуерисолутион**</span><span class="sxs-lookup"><span data-stu-id="290fa-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="290fa-144">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="290fa-144">Other Samples</span></span>

[<span data-ttu-id="290fa-145">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="290fa-145">Search Code Samples</span></span>](-search-samples-ovw.md)
