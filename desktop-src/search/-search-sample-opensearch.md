---
description: Пример кода OpenSearch демонстрирует создание федеративной службы поиска с помощью протокола OpenSearch и файла дескриптора OpenSearch (. OSDX-) (соединителя поиска).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423726"
---
# <a name="opensearch"></a><span data-ttu-id="28740-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="28740-103">OpenSearch</span></span>

<span data-ttu-id="28740-104">Пример кода OpenSearch демонстрирует создание федеративной службы поиска с помощью протокола [OpenSearch](https://github.com/dewitt/opensearch) и файла дескриптора OpenSearch (. OSDX-) (соединителя поиска).</span><span class="sxs-lookup"><span data-stu-id="28740-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="28740-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="28740-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="28740-106">Требования</span><span class="sxs-lookup"><span data-stu-id="28740-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="28740-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="28740-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="28740-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="28740-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="28740-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="28740-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="28740-110">См. также</span><span class="sxs-lookup"><span data-stu-id="28740-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="28740-111">Требования</span><span class="sxs-lookup"><span data-stu-id="28740-111">Requirements</span></span>



| <span data-ttu-id="28740-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="28740-112">Product</span></span>     | <span data-ttu-id="28740-113">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="28740-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="28740-114">Windows</span><span class="sxs-lookup"><span data-stu-id="28740-114">Windows</span></span>     | <span data-ttu-id="28740-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28740-115">Windows 7</span></span>               |
| <span data-ttu-id="28740-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="28740-116">Windows SDK</span></span> | <span data-ttu-id="28740-117">7.0</span><span class="sxs-lookup"><span data-stu-id="28740-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="28740-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="28740-118">Downloading the Sample</span></span>

<span data-ttu-id="28740-119">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="28740-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="28740-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="28740-120">Location</span></span>      | <span data-ttu-id="28740-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="28740-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="28740-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="28740-122">GitHub</span></span>  | [<span data-ttu-id="28740-123">Пример OpenSearch</span><span class="sxs-lookup"><span data-stu-id="28740-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="28740-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="28740-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="28740-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="28740-125">Building the Sample</span></span>

<span data-ttu-id="28740-126">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="28740-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="28740-127">Откройте окно командной строки и перейдите в каталог проекта **адвентуресеарч** .</span><span class="sxs-lookup"><span data-stu-id="28740-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="28740-128">Введите `msbuild AdventureSearch.sln`.</span><span class="sxs-lookup"><span data-stu-id="28740-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="28740-129">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="28740-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="28740-130">Откройте проводник Windows и перейдите в каталог проекта **адвентуресеарч** .</span><span class="sxs-lookup"><span data-stu-id="28740-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="28740-131">Дважды щелкните значок файла Адвентуресеарч. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="28740-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="28740-132">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28740-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="28740-133">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="28740-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="28740-134">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="28740-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="28740-135">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="28740-135">Running the Sample</span></span>

1.  <span data-ttu-id="28740-136">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="28740-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="28740-137">В командной строке введите `AdventureSearch.exe` или в проводнике Windows дважды щелкните значок AdventureSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="28740-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="28740-138">В командной строке введите `GetOSDX.exe` или в проводнике Windows дважды щелкните значок GetOSDX.exe.</span><span class="sxs-lookup"><span data-stu-id="28740-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28740-139">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="28740-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="28740-140">**Reference**</span><span class="sxs-lookup"><span data-stu-id="28740-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28740-141">Обзор схемы описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="28740-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="28740-142">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="28740-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28740-143">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="28740-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="28740-144">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="28740-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="28740-145">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="28740-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="28740-146">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="28740-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 
