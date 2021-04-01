---
title: Пользовательский пример интерполяции
description: Показывает, как использовать анимацию Windows с собственным пользовательским интерполяцией с Direct2D, используемой для отрисовки.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "104133627"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="79fc0-103">Пользовательский пример интерполяции</span><span class="sxs-lookup"><span data-stu-id="79fc0-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="79fc0-104">Показывает, как использовать анимацию Windows с собственным пользовательским интерполяцией с Direct2D, используемой для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="79fc0-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="79fc0-105">Образцы изображений загружаются из библиотеки рисунков.</span><span class="sxs-lookup"><span data-stu-id="79fc0-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="79fc0-106">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="79fc0-106">Downloading the Sample</span></span>

<span data-ttu-id="79fc0-107">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="79fc0-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="79fc0-108">Расположение</span><span class="sxs-lookup"><span data-stu-id="79fc0-108">Location</span></span>                               | <span data-ttu-id="79fc0-109">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="79fc0-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79fc0-110">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="79fc0-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="79fc0-111">Пакет средств разработки программного обеспечения Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="79fc0-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="79fc0-112">Коллекция кодов</span><span class="sxs-lookup"><span data-stu-id="79fc0-112">Code Gallery</span></span>                           | [<span data-ttu-id="79fc0-113">Пример кода для диспетчера анимации Windows</span><span class="sxs-lookup"><span data-stu-id="79fc0-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="79fc0-114">После загрузки и установки Windows SDK вы найдете образцы в каталоге установки.</span><span class="sxs-lookup"><span data-stu-id="79fc0-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="79fc0-115">Например, если вы используете путь установки по умолчанию для Windows SDK для Windows 7, образцы устанавливаются на диске C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="79fc0-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="79fc0-116">Построение образца</span><span class="sxs-lookup"><span data-stu-id="79fc0-116">Building the Sample</span></span>

<span data-ttu-id="79fc0-117">Для построения образца используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="79fc0-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="79fc0-118">**Построение примера в командной строке**</span><span class="sxs-lookup"><span data-stu-id="79fc0-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="79fc0-119">Откройте окно командной строки и перейдите в каталог проекта Кустоминтерполатор.</span><span class="sxs-lookup"><span data-stu-id="79fc0-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="79fc0-120">Например, путь установки по умолчанию для этого образца — C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ мультимедиа \\ виндовсаниматион \\ кустоминтерполатор</span><span class="sxs-lookup"><span data-stu-id="79fc0-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="79fc0-121">Выполните следующую команду: **MSBuild кустоминтерполатор. sln.**</span><span class="sxs-lookup"><span data-stu-id="79fc0-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="79fc0-122">**Построение примера с помощью Microsoft Visual Studio (предпочтительно)**</span><span class="sxs-lookup"><span data-stu-id="79fc0-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="79fc0-123">Откройте проводник Windows и перейдите в каталог проекта Кустоминтерполатор.</span><span class="sxs-lookup"><span data-stu-id="79fc0-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="79fc0-124">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79fc0-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="79fc0-125">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="79fc0-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="79fc0-126">Дважды щелкните значок файла Кустоминтерполатор. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="79fc0-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="79fc0-127">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="79fc0-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="79fc0-128">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="79fc0-128">Running the Sample</span></span>

<span data-ttu-id="79fc0-129">Запуск примера:</span><span class="sxs-lookup"><span data-stu-id="79fc0-129">To run the sample:</span></span>

1.  <span data-ttu-id="79fc0-130">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="79fc0-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="79fc0-131">Запустите **CustomInterpolator.exe** из командной строки или дважды щелкните значок для CustomInterpolator.exe в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="79fc0-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="79fc0-132">Измените размер окна или нажмите клавишу пробел, и изображения будут произвольно расположиться в середине клиентской области.</span><span class="sxs-lookup"><span data-stu-id="79fc0-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="79fc0-133">Нажмите кнопку со стрелкой вверх или вниз. изображения будут ускорены в верхней или нижней части клиентской области.</span><span class="sxs-lookup"><span data-stu-id="79fc0-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 




