---
description: Демонстрирует создание команды, которая работает с выбранным элементом оболочки или контейнером для создания списка воспроизведения.
title: 'Пример: создание списка воспроизведения'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986121"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="48868-103">Пример: создание списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="48868-103">Playlist Creator Sample</span></span>

<span data-ttu-id="48868-104">Демонстрирует создание команды, которая работает с выбранным элементом оболочки или контейнером для создания списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="48868-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="48868-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="48868-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="48868-106">Требования</span><span class="sxs-lookup"><span data-stu-id="48868-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="48868-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="48868-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="48868-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="48868-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="48868-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="48868-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="48868-110">Требования</span><span class="sxs-lookup"><span data-stu-id="48868-110">Requirements</span></span>



| <span data-ttu-id="48868-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="48868-111">Product</span></span>                                | <span data-ttu-id="48868-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="48868-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="48868-113">Windows</span><span class="sxs-lookup"><span data-stu-id="48868-113">Windows</span></span>                                | <span data-ttu-id="48868-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48868-114">Windows Vista</span></span>           |
| <span data-ttu-id="48868-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="48868-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="48868-116">7.0</span><span class="sxs-lookup"><span data-stu-id="48868-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="48868-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="48868-117">Downloading the Sample</span></span>

| <span data-ttu-id="48868-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="48868-118">Location</span></span>      | <span data-ttu-id="48868-119">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="48868-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48868-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="48868-120">GitHub</span></span>  | [<span data-ttu-id="48868-121">Пример Плайлисткреатор</span><span class="sxs-lookup"><span data-stu-id="48868-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="48868-122">Построение образца</span><span class="sxs-lookup"><span data-stu-id="48868-122">Building the Sample</span></span>

<span data-ttu-id="48868-123">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="48868-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="48868-124">Откройте окно командной строки и перейдите в каталог проекта **плайлисткреатор** .</span><span class="sxs-lookup"><span data-stu-id="48868-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="48868-125">Введите `msbuild PlaylistCreator.sln`.</span><span class="sxs-lookup"><span data-stu-id="48868-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="48868-126">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="48868-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="48868-127">Этот образец можно также использовать с Visual C++ Express Edition, если полная версия Visual Studio недоступна.</span><span class="sxs-lookup"><span data-stu-id="48868-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="48868-128">Откройте проводник Windows и перейдите в каталог проекта **плайлисткреатор** .</span><span class="sxs-lookup"><span data-stu-id="48868-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="48868-129">Дважды щелкните значок файла Плайлисткреатор. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="48868-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="48868-130">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="48868-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="48868-131">При компиляции 64-bit с помощью Visual C++ Express Edition необходимо использовать кросс-компилятор x64, предоставляемый вместе с Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="48868-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="48868-132">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="48868-132">Running the Sample</span></span>

1.  <span data-ttu-id="48868-133">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="48868-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="48868-134">В командной строке введите `PlaylistCreator.exe` .</span><span class="sxs-lookup"><span data-stu-id="48868-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="48868-135">Кроме того, в проводнике Windows дважды щелкните значок PlaylistCreator.exe.</span><span class="sxs-lookup"><span data-stu-id="48868-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="48868-136">Щелкните правой кнопкой мыши любой музыкальный файл или папку с музыкальными файлами в проводнике Windows, чтобы создать список воспроизведения, чтобы открыть контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="48868-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="48868-137">Вы можете создать список воспроизведения M3U или WPL.</span><span class="sxs-lookup"><span data-stu-id="48868-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="48868-138">Списки воспроизведения создаются в `%userprofile%\Music\Playlists` папке.</span><span class="sxs-lookup"><span data-stu-id="48868-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="48868-139">Новые команды в контекстном меню можно найти в папке « **музыка** », в стеках музыки, в стопках в **музыкальной библиотеке** и коллекциях музыкальных файлов.</span><span class="sxs-lookup"><span data-stu-id="48868-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 



