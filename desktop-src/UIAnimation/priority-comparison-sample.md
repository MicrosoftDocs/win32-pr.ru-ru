---
title: Пример сравнения приоритетов
description: Показывает, как использовать анимацию Windows с собственным сравнением приоритетов с помощью Direct2D для подготовки к просмотру.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "104133626"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="a8f69-103">Пример сравнения приоритетов</span><span class="sxs-lookup"><span data-stu-id="a8f69-103">Priority Comparison Sample</span></span>

<span data-ttu-id="a8f69-104">Показывает, как использовать анимацию Windows с собственным сравнением приоритетов с помощью Direct2D для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="a8f69-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a8f69-105">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a8f69-105">Downloading the Sample</span></span>

<span data-ttu-id="a8f69-106">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="a8f69-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="a8f69-107">Расположение</span><span class="sxs-lookup"><span data-stu-id="a8f69-107">Location</span></span>                               | <span data-ttu-id="a8f69-108">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="a8f69-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f69-109">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a8f69-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="a8f69-110">Пакет средств разработки программного обеспечения Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="a8f69-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="a8f69-111">Коллекция кодов</span><span class="sxs-lookup"><span data-stu-id="a8f69-111">Code Gallery</span></span>                           | [<span data-ttu-id="a8f69-112">Пример кода для диспетчера анимации Windows</span><span class="sxs-lookup"><span data-stu-id="a8f69-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="a8f69-113">После загрузки и установки Windows SDK вы найдете образцы в каталоге установки.</span><span class="sxs-lookup"><span data-stu-id="a8f69-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="a8f69-114">Например, если вы используете путь установки по умолчанию для Windows SDK для Windows 7, образцы устанавливаются на диске C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="a8f69-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="a8f69-115">Построение образца</span><span class="sxs-lookup"><span data-stu-id="a8f69-115">Building the Sample</span></span>

<span data-ttu-id="a8f69-116">Для построения образца используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="a8f69-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="a8f69-117">**Построение примера в командной строке**</span><span class="sxs-lookup"><span data-stu-id="a8f69-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="a8f69-118">Откройте окно командной строки и перейдите в каталог проекта Приоритикомпарисон.</span><span class="sxs-lookup"><span data-stu-id="a8f69-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="a8f69-119">Например, путь установки по умолчанию для этого образца — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ мультимедиа \\ виндовсаниматион \\ приоритикомпарисон.</span><span class="sxs-lookup"><span data-stu-id="a8f69-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="a8f69-120">Выполните следующую команду: **MSBuild приоритикомпарисон. sln.**</span><span class="sxs-lookup"><span data-stu-id="a8f69-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="a8f69-121">**Построение примера с помощью Microsoft Visual Studio (предпочтительно)**</span><span class="sxs-lookup"><span data-stu-id="a8f69-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="a8f69-122">Откройте проводник Windows и перейдите в каталог проекта Приоритикомпарисон.</span><span class="sxs-lookup"><span data-stu-id="a8f69-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="a8f69-123">Дважды щелкните значок файла Приоритикомпарисон. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a8f69-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="a8f69-124">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8f69-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="a8f69-125">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="a8f69-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="a8f69-126">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="a8f69-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a8f69-127">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a8f69-127">Running the Sample</span></span>

<span data-ttu-id="a8f69-128">Запуск примера:</span><span class="sxs-lookup"><span data-stu-id="a8f69-128">To run the sample:</span></span>

1.  <span data-ttu-id="a8f69-129">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="a8f69-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="a8f69-130">Запустите **PriorityComparison.exe** из командной строки или дважды щелкните значок для PriorityComparison.exe в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="a8f69-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="a8f69-131">Образцы изображений загружаются из библиотеки рисунков.</span><span class="sxs-lookup"><span data-stu-id="a8f69-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="a8f69-132">Измените размер окна или нажмите клавишу пробел, и изображения будут перемещены в центр.</span><span class="sxs-lookup"><span data-stu-id="a8f69-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="a8f69-133">Используйте клавиши со стрелками влево и вправо для выбора различных изображений (чем быстрее нажата клавиша, тем быстрее будет изменяться выбор).</span><span class="sxs-lookup"><span data-stu-id="a8f69-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="a8f69-134">Используйте клавиши со стрелками вверх и вниз для создания волнового изображения (чем быстрее клавиша нажата, тем быстрее волна).</span><span class="sxs-lookup"><span data-stu-id="a8f69-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 




