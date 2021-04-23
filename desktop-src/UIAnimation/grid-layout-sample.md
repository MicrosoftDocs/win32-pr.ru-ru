---
title: Образец макета сетки
description: Показывает, как использовать анимацию Windows с помощью Direct2D для анимации сетки изображений.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "103789420"
---
# <a name="grid-layout-sample"></a><span data-ttu-id="51119-103">Образец макета сетки</span><span class="sxs-lookup"><span data-stu-id="51119-103">Grid Layout Sample</span></span>

<span data-ttu-id="51119-104">Показывает, как использовать анимацию Windows с помощью Direct2D для анимации сетки изображений.</span><span class="sxs-lookup"><span data-stu-id="51119-104">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="51119-105">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="51119-105">Downloading the Sample</span></span>

<span data-ttu-id="51119-106">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="51119-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="51119-107">Расположение</span><span class="sxs-lookup"><span data-stu-id="51119-107">Location</span></span>                               | <span data-ttu-id="51119-108">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="51119-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51119-109">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="51119-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="51119-110">Пакет средств разработки программного обеспечения Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="51119-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="51119-111">Коллекция кодов</span><span class="sxs-lookup"><span data-stu-id="51119-111">Code Gallery</span></span>                           | [<span data-ttu-id="51119-112">Пример кода для диспетчера анимации Windows</span><span class="sxs-lookup"><span data-stu-id="51119-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="51119-113">После загрузки и установки Windows SDK вы найдете образцы в каталоге установки.</span><span class="sxs-lookup"><span data-stu-id="51119-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="51119-114">Например, если вы используете путь установки по умолчанию для Windows SDK для Windows 7, образцы устанавливаются на диске C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="51119-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="51119-115">Построение образца</span><span class="sxs-lookup"><span data-stu-id="51119-115">Building the Sample</span></span>

<span data-ttu-id="51119-116">Для построения образца используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="51119-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="51119-117">**Построение примера в командной строке**</span><span class="sxs-lookup"><span data-stu-id="51119-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="51119-118">Откройте окно командной строки и перейдите в каталог проекта GridLayout.</span><span class="sxs-lookup"><span data-stu-id="51119-118">Open the Command Prompt window and navigate to the GridLayout project directory.</span></span> <span data-ttu-id="51119-119">Например, путь установки по умолчанию для этого образца — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ мультимедиа \\ виндовсаниматион \\ GridLayout</span><span class="sxs-lookup"><span data-stu-id="51119-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\GridLayout</span></span>

2.  <span data-ttu-id="51119-120">Выполните следующую команду: **MSBuild GridLayout. sln**</span><span class="sxs-lookup"><span data-stu-id="51119-120">Run the following command: **msbuild GridLayout.sln**</span></span>

<span data-ttu-id="51119-121">**Построение примера с помощью Microsoft Visual Studio (предпочтительно)**</span><span class="sxs-lookup"><span data-stu-id="51119-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="51119-122">Откройте проводник Windows и перейдите к каталогу проекта GridLayout.</span><span class="sxs-lookup"><span data-stu-id="51119-122">Open Windows Explorer and navigate to the GridLayout project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="51119-123">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51119-123">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="51119-124">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="51119-124">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="51119-125">Дважды щелкните значок файла GridLayout. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="51119-125">Double-click the icon for the GridLayout.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="51119-126">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="51119-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="51119-127">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="51119-127">Running the Sample</span></span>

<span data-ttu-id="51119-128">Запуск примера:</span><span class="sxs-lookup"><span data-stu-id="51119-128">To run the sample:</span></span>

1.  <span data-ttu-id="51119-129">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="51119-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="51119-130">Запустите **GridLayout.exe** из командной строки или дважды щелкните значок для GridLayout.exe в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="51119-130">Run **GridLayout.exe** at the command prompt, or double-click the icon for GridLayout.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="51119-131">Образцы изображений загружаются из библиотеки рисунков.</span><span class="sxs-lookup"><span data-stu-id="51119-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="51119-132">Измените размер окна, и изображения будут размещаться в сетке.</span><span class="sxs-lookup"><span data-stu-id="51119-132">Resize the window and the images will arrange themselves into a grid.</span></span>

 

 




