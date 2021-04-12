---
title: Пример анимации Timer-Driven
description: Показывает, как использовать анимацию Windows с таймером анимации, а также с помощью GDI+ для анимации цвета фона окна.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "104336740"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="1f3a7-103">Пример анимации Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="1f3a7-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="1f3a7-104">Показывает, как использовать анимацию Windows с таймером анимации, а также с помощью GDI+ для анимации цвета фона окна.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="1f3a7-105">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="1f3a7-105">Downloading the Sample</span></span>

<span data-ttu-id="1f3a7-106">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="1f3a7-107">Расположение</span><span class="sxs-lookup"><span data-stu-id="1f3a7-107">Location</span></span>                               | <span data-ttu-id="1f3a7-108">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="1f3a7-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3a7-109">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1f3a7-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="1f3a7-110">Пакет средств разработки программного обеспечения Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="1f3a7-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="1f3a7-111">Коллекция кодов</span><span class="sxs-lookup"><span data-stu-id="1f3a7-111">Code Gallery</span></span>                           | [<span data-ttu-id="1f3a7-112">Пример кода для диспетчера анимации Windows</span><span class="sxs-lookup"><span data-stu-id="1f3a7-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="1f3a7-113">После загрузки и установки Windows SDK вы найдете образцы в каталоге установки.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="1f3a7-114">Например, если вы используете путь установки по умолчанию для Windows SDK для Windows 7, образцы устанавливаются на диске C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="1f3a7-115">Построение образца</span><span class="sxs-lookup"><span data-stu-id="1f3a7-115">Building the Sample</span></span>

<span data-ttu-id="1f3a7-116">Для построения образца используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="1f3a7-117">**Построение примера в командной строке**</span><span class="sxs-lookup"><span data-stu-id="1f3a7-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="1f3a7-118">Откройте окно командной строки и перейдите в каталог проекта Тимердривен.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="1f3a7-119">Например, путь установки по умолчанию для этого образца — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ мультимедиа \\ виндовсаниматион \\ тимердривен.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="1f3a7-120">Выполните следующую команду: **MSBuild тимердривен. sln.**</span><span class="sxs-lookup"><span data-stu-id="1f3a7-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="1f3a7-121">**Построение примера с помощью Microsoft Visual Studio (предпочтительно)**</span><span class="sxs-lookup"><span data-stu-id="1f3a7-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="1f3a7-122">Откройте проводник Windows и перейдите в каталог проекта Тимердривен.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="1f3a7-123">Дважды щелкните значок файла Тимердривен. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="1f3a7-124">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="1f3a7-125">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="1f3a7-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="1f3a7-126">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1f3a7-127">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="1f3a7-127">Running the Sample</span></span>

<span data-ttu-id="1f3a7-128">Запуск примера:</span><span class="sxs-lookup"><span data-stu-id="1f3a7-128">To run the sample:</span></span>

1.  <span data-ttu-id="1f3a7-129">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="1f3a7-130">Запустите **TimerDriven.exe** из командной строки или дважды щелкните значок для TimerDriven.exe в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="1f3a7-131">Щелкните в любом месте клиентской области, и цвет фона окна изменится на случайный цвет.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




