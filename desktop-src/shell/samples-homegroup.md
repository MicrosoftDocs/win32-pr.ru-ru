---
description: Показывает, как определить состояние членства в домашней группе, перечислить элементы верхнего уровня в папке оболочки домашней группы и запустить мастер общего доступа к домашней группе.
title: Пример HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080952"
---
# <a name="homegroup-sample"></a><span data-ttu-id="5bac2-103">Пример HomeGroup</span><span class="sxs-lookup"><span data-stu-id="5bac2-103">HomeGroup Sample</span></span>

<span data-ttu-id="5bac2-104">Показывает, как определить состояние членства в домашней группе, перечислить элементы верхнего уровня в папке оболочки **домашней группы** и запустить **мастер общего доступа к домашней группе**.</span><span class="sxs-lookup"><span data-stu-id="5bac2-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="5bac2-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5bac2-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5bac2-106">Требования</span><span class="sxs-lookup"><span data-stu-id="5bac2-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5bac2-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="5bac2-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="5bac2-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="5bac2-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="5bac2-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="5bac2-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="5bac2-110">См. также</span><span class="sxs-lookup"><span data-stu-id="5bac2-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="5bac2-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5bac2-111">Requirements</span></span>



| <span data-ttu-id="5bac2-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="5bac2-112">Product</span></span>                                | <span data-ttu-id="5bac2-113">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="5bac2-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="5bac2-114">Windows</span><span class="sxs-lookup"><span data-stu-id="5bac2-114">Windows</span></span>                                | <span data-ttu-id="5bac2-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5bac2-115">Windows 7</span></span>               |
| <span data-ttu-id="5bac2-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="5bac2-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="5bac2-117">7.0</span><span class="sxs-lookup"><span data-stu-id="5bac2-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="5bac2-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="5bac2-118">Downloading the Sample</span></span>

| <span data-ttu-id="5bac2-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="5bac2-119">Location</span></span>      | <span data-ttu-id="5bac2-120">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="5bac2-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bac2-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="5bac2-121">GitHub</span></span>  | [<span data-ttu-id="5bac2-122">Пример домашней группы</span><span class="sxs-lookup"><span data-stu-id="5bac2-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="5bac2-123">Построение образца</span><span class="sxs-lookup"><span data-stu-id="5bac2-123">Building the Sample</span></span>

<span data-ttu-id="5bac2-124">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5bac2-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="5bac2-125">Откройте окно командной строки и перейдите в каталог проекта **домашней группы** .</span><span class="sxs-lookup"><span data-stu-id="5bac2-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="5bac2-126">Введите `msbuild HomeGroup.sln`.</span><span class="sxs-lookup"><span data-stu-id="5bac2-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="5bac2-127">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="5bac2-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="5bac2-128">Откройте проводник Windows и перейдите к каталогу проекта **домашней группы** .</span><span class="sxs-lookup"><span data-stu-id="5bac2-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="5bac2-129">Дважды щелкните значок файла Домашняя группа. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5bac2-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="5bac2-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="5bac2-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5bac2-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="5bac2-131">Running the Sample</span></span>

1.  <span data-ttu-id="5bac2-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="5bac2-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="5bac2-133">В командной строке введите `HomeGroup.exe` .</span><span class="sxs-lookup"><span data-stu-id="5bac2-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="5bac2-134">Кроме того, в проводнике Windows дважды щелкните значок HomeGroup.exe.</span><span class="sxs-lookup"><span data-stu-id="5bac2-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bac2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5bac2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bac2-136">**ихомеграуп**</span><span class="sxs-lookup"><span data-stu-id="5bac2-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="5bac2-137">**кновнфолдерид**</span><span class="sxs-lookup"><span data-stu-id="5bac2-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 



