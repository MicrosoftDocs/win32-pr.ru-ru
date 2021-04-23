---
description: В образце кода Сеарчевентс показано, как задать приоритет событий индексирования.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: сеарчевентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692190"
---
# <a name="searchevents"></a><span data-ttu-id="502b9-103">сеарчевентс</span><span class="sxs-lookup"><span data-stu-id="502b9-103">SearchEvents</span></span>

<span data-ttu-id="502b9-104">В образце кода Сеарчевентс показано, как задать приоритет событий индексирования.</span><span class="sxs-lookup"><span data-stu-id="502b9-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="502b9-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="502b9-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="502b9-106">Требования</span><span class="sxs-lookup"><span data-stu-id="502b9-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="502b9-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="502b9-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="502b9-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="502b9-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="502b9-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="502b9-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="502b9-110">См. также</span><span class="sxs-lookup"><span data-stu-id="502b9-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="502b9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="502b9-111">Requirements</span></span>

| <span data-ttu-id="502b9-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="502b9-112">Product</span></span>     | <span data-ttu-id="502b9-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="502b9-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="502b9-114">Windows</span><span class="sxs-lookup"><span data-stu-id="502b9-114">Windows</span></span>     | <span data-ttu-id="502b9-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="502b9-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="502b9-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="502b9-116">Windows SDK</span></span> | <span data-ttu-id="502b9-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="502b9-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="502b9-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="502b9-118">Downloading the Sample</span></span>

<span data-ttu-id="502b9-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="502b9-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="502b9-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="502b9-120">Location</span></span>      | <span data-ttu-id="502b9-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="502b9-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="502b9-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="502b9-122">GitHub</span></span>        | [<span data-ttu-id="502b9-123">Пример Сеарчевентс</span><span class="sxs-lookup"><span data-stu-id="502b9-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="502b9-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="502b9-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="502b9-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="502b9-125">Building the Sample</span></span>

1. <span data-ttu-id="502b9-126">Откройте проводник Windows и перейдите в каталог проекта **сеарчевентс** .</span><span class="sxs-lookup"><span data-stu-id="502b9-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="502b9-127">Дважды щелкните значок файла Eventing. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="502b9-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="502b9-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="502b9-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="502b9-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="502b9-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="502b9-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="502b9-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="502b9-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="502b9-131">Running the Sample</span></span>

1. <span data-ttu-id="502b9-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="502b9-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="502b9-133">В командной строке введите `Eventing.exe` или в проводнике Windows дважды щелкните значок Eventing.exe.</span><span class="sxs-lookup"><span data-stu-id="502b9-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="502b9-134">См. также</span><span class="sxs-lookup"><span data-stu-id="502b9-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="502b9-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="502b9-135">Reference</span></span>

[<span data-ttu-id="502b9-136">**ировсетевентс**</span><span class="sxs-lookup"><span data-stu-id="502b9-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="502b9-137">**ировсетприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="502b9-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="502b9-138">**уровень ПРИОРИТЕТа \_**</span><span class="sxs-lookup"><span data-stu-id="502b9-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="502b9-139">**РОВСЕТЕВЕНТ \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="502b9-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="502b9-140">**\_тип ровсетевент**</span><span class="sxs-lookup"><span data-stu-id="502b9-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="502b9-141">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="502b9-141">Other Samples</span></span>

[<span data-ttu-id="502b9-142">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="502b9-142">Search Code Samples</span></span>](-search-samples-ovw.md)
