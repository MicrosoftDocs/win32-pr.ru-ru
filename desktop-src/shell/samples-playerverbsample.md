---
description: Демонстрирует создание команды, которая работает с элементами оболочки и контейнерами, которая воспроизводит элементы или добавляет элементы в очередь.
title: 'Пример: команда проигрывателя'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264899"
---
# <a name="player-verb-sample"></a><span data-ttu-id="db4eb-103">Пример: команда проигрывателя</span><span class="sxs-lookup"><span data-stu-id="db4eb-103">Player Verb Sample</span></span>

<span data-ttu-id="db4eb-104">Демонстрирует создание команды, которая работает с элементами оболочки и контейнерами, которая воспроизводит элементы или добавляет элементы в очередь.</span><span class="sxs-lookup"><span data-stu-id="db4eb-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="db4eb-105">Этот пример особенно полезен для мультимедийных приложений.</span><span class="sxs-lookup"><span data-stu-id="db4eb-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="db4eb-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="db4eb-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="db4eb-107">Требования</span><span class="sxs-lookup"><span data-stu-id="db4eb-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="db4eb-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="db4eb-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="db4eb-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="db4eb-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="db4eb-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="db4eb-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="db4eb-111">Требования</span><span class="sxs-lookup"><span data-stu-id="db4eb-111">Requirements</span></span>



| <span data-ttu-id="db4eb-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="db4eb-112">Product</span></span>                                | <span data-ttu-id="db4eb-113">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="db4eb-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="db4eb-114">Windows</span><span class="sxs-lookup"><span data-stu-id="db4eb-114">Windows</span></span>                                | <span data-ttu-id="db4eb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db4eb-115">Windows Vista</span></span>           |
| <span data-ttu-id="db4eb-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="db4eb-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="db4eb-117">7.0</span><span class="sxs-lookup"><span data-stu-id="db4eb-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="db4eb-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="db4eb-118">Downloading the Sample</span></span>

| <span data-ttu-id="db4eb-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="db4eb-119">Location</span></span>      | <span data-ttu-id="db4eb-120">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="db4eb-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db4eb-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="db4eb-121">GitHub</span></span>  | [<span data-ttu-id="db4eb-122">Пример Плайерверб</span><span class="sxs-lookup"><span data-stu-id="db4eb-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="db4eb-123">Построение образца</span><span class="sxs-lookup"><span data-stu-id="db4eb-123">Building the Sample</span></span>

<span data-ttu-id="db4eb-124">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="db4eb-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="db4eb-125">Откройте окно командной строки и перейдите в каталог проекта **плайервербсампле** .</span><span class="sxs-lookup"><span data-stu-id="db4eb-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="db4eb-126">Введите `msbuild PlayerVerbSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="db4eb-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="db4eb-127">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="db4eb-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="db4eb-128">Откройте проводник Windows и перейдите в каталог проекта **плайервербсампле** .</span><span class="sxs-lookup"><span data-stu-id="db4eb-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="db4eb-129">Дважды щелкните значок файла Плайервербсампле. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="db4eb-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="db4eb-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="db4eb-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="db4eb-131">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="db4eb-131">Running the Sample</span></span>

1.  <span data-ttu-id="db4eb-132">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="db4eb-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="db4eb-133">В командной строке введите `PlayerVerbSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="db4eb-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="db4eb-134">Кроме того, в проводнике Windows дважды щелкните значок PlayerVerbSample.exe.</span><span class="sxs-lookup"><span data-stu-id="db4eb-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="db4eb-135">Выберите `Register Verbs` в диалоговом окне **Пример команды проигрывателя** .</span><span class="sxs-lookup"><span data-stu-id="db4eb-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="db4eb-136">Щелкните правой кнопкой мыши элемент изображения (файл, папка или стек) в проводнике Windows, чтобы добавить их в очередь или воспроизвести в примере приложения.</span><span class="sxs-lookup"><span data-stu-id="db4eb-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="db4eb-137">Используйте музыкальные элементы при изменении образца для работы с музыкой.</span><span class="sxs-lookup"><span data-stu-id="db4eb-137">Use music items when you change the sample to work with music.</span></span>

 

 



