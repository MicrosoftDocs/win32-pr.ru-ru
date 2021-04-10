---
description: Пример кода Всоледб демонстрирует использование библиотеки ATL OLE DB доступ к приложениям Windows Search и демонстрирует два дополнительных метода получения результатов из службы поиска Windows.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: всоледб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896930"
---
# <a name="wsoledb"></a><span data-ttu-id="36a30-103">всоледб</span><span class="sxs-lookup"><span data-stu-id="36a30-103">WSOleDB</span></span>

<span data-ttu-id="36a30-104">Пример кода Всоледб демонстрирует использование библиотеки ATL OLE DB доступ к приложениям Windows Search и демонстрирует два дополнительных метода получения результатов из службы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="36a30-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="36a30-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="36a30-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="36a30-106">Требования</span><span class="sxs-lookup"><span data-stu-id="36a30-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="36a30-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="36a30-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="36a30-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="36a30-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="36a30-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="36a30-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="36a30-110">См. также</span><span class="sxs-lookup"><span data-stu-id="36a30-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="36a30-111">Требования</span><span class="sxs-lookup"><span data-stu-id="36a30-111">Requirements</span></span>

| <span data-ttu-id="36a30-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="36a30-112">Product</span></span>     | <span data-ttu-id="36a30-113">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="36a30-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="36a30-114">Windows</span><span class="sxs-lookup"><span data-stu-id="36a30-114">Windows</span></span>     | <span data-ttu-id="36a30-115">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="36a30-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="36a30-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="36a30-116">Windows SDK</span></span> | <span data-ttu-id="36a30-117">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="36a30-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="36a30-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="36a30-118">Downloading the Sample</span></span>

<span data-ttu-id="36a30-119">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="36a30-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="36a30-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="36a30-120">Location</span></span>      | <span data-ttu-id="36a30-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="36a30-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="36a30-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="36a30-122">GitHub</span></span>        | [<span data-ttu-id="36a30-123">Пример Всоледб</span><span class="sxs-lookup"><span data-stu-id="36a30-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="36a30-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="36a30-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="36a30-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="36a30-125">Building the Sample</span></span>

1. <span data-ttu-id="36a30-126">Откройте проводник Windows и перейдите в каталог проекта **всоледб** .</span><span class="sxs-lookup"><span data-stu-id="36a30-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="36a30-127">Дважды щелкните значок файла Всоледб. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="36a30-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="36a30-128">Файл SLN был создан в более старой версии Visual Studio, поэтому его обновление потребуется, если используется Visual Studio 2012 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="36a30-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="36a30-129">Это не повлияет на поведение образца.</span><span class="sxs-lookup"><span data-stu-id="36a30-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="36a30-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="36a30-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="36a30-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="36a30-131">Running the Sample</span></span>

1. <span data-ttu-id="36a30-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="36a30-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="36a30-133">В командной строке введите `WSOleDB.exe` или в проводнике Windows дважды щелкните значок WSOleDB.exe.</span><span class="sxs-lookup"><span data-stu-id="36a30-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36a30-134">См. также</span><span class="sxs-lookup"><span data-stu-id="36a30-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="36a30-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="36a30-135">Reference</span></span>

[<span data-ttu-id="36a30-136">**исеарчкаталогманажер**</span><span class="sxs-lookup"><span data-stu-id="36a30-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="36a30-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="36a30-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="36a30-138">**исеарчманажер**</span><span class="sxs-lookup"><span data-stu-id="36a30-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="36a30-139">**ипропертисторе**</span><span class="sxs-lookup"><span data-stu-id="36a30-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="36a30-140">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="36a30-140">Conceptual</span></span>

[<span data-ttu-id="36a30-141">Общие сведения о программировании OLE DB</span><span class="sxs-lookup"><span data-stu-id="36a30-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="36a30-142">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="36a30-142">Other Samples</span></span>

[<span data-ttu-id="36a30-143">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="36a30-143">Search Code Samples</span></span>](-search-samples-ovw.md)
