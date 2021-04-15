---
description: Демонстрируется, как приложение может предоставить несколько целевых объектов переключения (как для вкладок) в таскбанд и как предоставить их эскизы.
title: Пример TabThumbnails
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986033"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="7c9e1-103">Пример TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="7c9e1-103">TabThumbnails Sample</span></span>

<span data-ttu-id="7c9e1-104">Демонстрируется, как приложение может предоставить несколько целевых объектов переключения (как для вкладок) в таскбанд и как предоставить их эскизы.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="7c9e1-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7c9e1-106">Требования</span><span class="sxs-lookup"><span data-stu-id="7c9e1-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7c9e1-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7c9e1-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7c9e1-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="7c9e1-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7c9e1-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7c9e1-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="7c9e1-110">Требования</span><span class="sxs-lookup"><span data-stu-id="7c9e1-110">Requirements</span></span>



| <span data-ttu-id="7c9e1-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="7c9e1-111">Product</span></span>                                | <span data-ttu-id="7c9e1-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="7c9e1-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="7c9e1-113">Windows</span><span class="sxs-lookup"><span data-stu-id="7c9e1-113">Windows</span></span>                                | <span data-ttu-id="7c9e1-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c9e1-114">Windows 7</span></span>               |
| <span data-ttu-id="7c9e1-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7c9e1-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="7c9e1-116">7.0</span><span class="sxs-lookup"><span data-stu-id="7c9e1-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7c9e1-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7c9e1-117">Downloading the Sample</span></span>

| <span data-ttu-id="7c9e1-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="7c9e1-118">Location</span></span>      | <span data-ttu-id="7c9e1-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="7c9e1-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9e1-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="7c9e1-120">GitHub</span></span>  | [<span data-ttu-id="7c9e1-121">Пример Табсумбнаилс</span><span class="sxs-lookup"><span data-stu-id="7c9e1-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="7c9e1-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="7c9e1-122">Building the Sample</span></span>

<span data-ttu-id="7c9e1-123">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7c9e1-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="7c9e1-124">Откройте окно командной строки и перейдите в каталог проекта **табсумбнаилс** .</span><span class="sxs-lookup"><span data-stu-id="7c9e1-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="7c9e1-125">Введите `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="7c9e1-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="7c9e1-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="7c9e1-127">Откройте проводник Windows и перейдите в каталог проекта **табсумбнаилс** .</span><span class="sxs-lookup"><span data-stu-id="7c9e1-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="7c9e1-128">Дважды щелкните значок файла Табсумбнаилс. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="7c9e1-129">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7c9e1-130">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="7c9e1-130">Running the Sample</span></span>

1.  <span data-ttu-id="7c9e1-131">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="7c9e1-132">В командной строке введите `TabThumbnails.exe` .</span><span class="sxs-lookup"><span data-stu-id="7c9e1-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="7c9e1-133">Кроме того, в проводнике Windows дважды щелкните значок TabThumbnails.exe.</span><span class="sxs-lookup"><span data-stu-id="7c9e1-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 



