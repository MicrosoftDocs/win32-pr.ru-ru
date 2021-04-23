---
title: Пример анимации Application-Driven
description: Показывает анимацию Windows в конфигурации, управляемой приложениями, с помощью Direct2D для анимации цвета фона окна и синхронизации с частотой обновления.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "105681594"
---
# <a name="application-driven-animation-sample"></a><span data-ttu-id="76fd5-103">Пример анимации Application-Driven</span><span class="sxs-lookup"><span data-stu-id="76fd5-103">Application-Driven Animation Sample</span></span>

<span data-ttu-id="76fd5-104">Показывает анимацию Windows в конфигурации, управляемой приложениями, с помощью Direct2D для анимации цвета фона окна и синхронизации с частотой обновления.</span><span class="sxs-lookup"><span data-stu-id="76fd5-104">Shows Windows Animation in the application-driven configuration by using Direct2D to animate the background color of a window and syncing to the refresh rate.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="76fd5-105">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="76fd5-105">Downloading the Sample</span></span>

<span data-ttu-id="76fd5-106">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="76fd5-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="76fd5-107">Расположение</span><span class="sxs-lookup"><span data-stu-id="76fd5-107">Location</span></span>                               | <span data-ttu-id="76fd5-108">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="76fd5-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fd5-109">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="76fd5-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="76fd5-110">Пакет средств разработки программного обеспечения Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="76fd5-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="76fd5-111">Коллекция кодов</span><span class="sxs-lookup"><span data-stu-id="76fd5-111">Code Gallery</span></span>                           | [<span data-ttu-id="76fd5-112">Пример кода для диспетчера анимации Windows</span><span class="sxs-lookup"><span data-stu-id="76fd5-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="76fd5-113">После загрузки и установки Windows SDK вы найдете образцы в каталоге установки.</span><span class="sxs-lookup"><span data-stu-id="76fd5-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="76fd5-114">Например, если вы используете путь установки по умолчанию для Windows SDK для Windows 7, образцы устанавливаются на диске C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="76fd5-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="76fd5-115">Построение образца</span><span class="sxs-lookup"><span data-stu-id="76fd5-115">Building the Sample</span></span>

<span data-ttu-id="76fd5-116">Для построения образца используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="76fd5-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="76fd5-117">**Построение примера в командной строке**</span><span class="sxs-lookup"><span data-stu-id="76fd5-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="76fd5-118">Откройте окно командной строки и перейдите в каталог проекта Аппдривен.</span><span class="sxs-lookup"><span data-stu-id="76fd5-118">Open the Command Prompt window and navigate to the AppDriven project directory.</span></span> <span data-ttu-id="76fd5-119">Например, путь установки по умолчанию для этого образца — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ мультимедиа \\ виндовсаниматион \\ аппдривен.</span><span class="sxs-lookup"><span data-stu-id="76fd5-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\AppDriven.</span></span>

2.  <span data-ttu-id="76fd5-120">Выполните следующую команду: **MSBuild аппдривен. sln.**</span><span class="sxs-lookup"><span data-stu-id="76fd5-120">Run the following command: **msbuild AppDriven.sln**</span></span>

<span data-ttu-id="76fd5-121">**Построение примера с помощью Microsoft Visual Studio (предпочтительно)**</span><span class="sxs-lookup"><span data-stu-id="76fd5-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="76fd5-122">Откройте проводник Windows и перейдите в каталог проекта Аппдривен.</span><span class="sxs-lookup"><span data-stu-id="76fd5-122">Open Windows Explorer and navigate to the AppDriven project directory.</span></span>

2.  <span data-ttu-id="76fd5-123">Дважды щелкните значок файла Аппдривен. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="76fd5-123">Double-click the icon for the AppDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="76fd5-124">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76fd5-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="76fd5-125">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="76fd5-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="76fd5-126">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="76fd5-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="76fd5-127">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="76fd5-127">Running the Sample</span></span>

<span data-ttu-id="76fd5-128">Запуск примера:</span><span class="sxs-lookup"><span data-stu-id="76fd5-128">To run the sample:</span></span>

1.  <span data-ttu-id="76fd5-129">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="76fd5-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="76fd5-130">Запустите **AppDriven.exe** из командной строки или дважды щелкните значок для AppDriven.exe в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="76fd5-130">Run **AppDriven.exe** at the command prompt, or double-click the icon for AppDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="76fd5-131">Щелкните в любом месте клиентской области, и цвет фона окна изменится на случайный цвет.</span><span class="sxs-lookup"><span data-stu-id="76fd5-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




