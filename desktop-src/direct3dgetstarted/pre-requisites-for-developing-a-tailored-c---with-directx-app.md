---
title: Необходимые условия для разработки с помощью DirectX
description: Когда вы начинаете разрабатывать приложение для Windows с помощью DirectX, не забывайте о необходимых условиях на этой странице. В их число входят те технологии, которые необходимо знать перед тем, как вы попытаетесь углубиться в.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Приложение DirectX, предварительные требования
- Приложение DirectX, приложение для Магазина Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2020
ms.locfileid: "104488610"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="10574-106">Необходимые условия для разработки с помощью DirectX</span><span class="sxs-lookup"><span data-stu-id="10574-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="10574-107">Когда вы начинаете разрабатывать приложение для Windows с помощью DirectX, не забывайте о необходимых условиях на этой странице.</span><span class="sxs-lookup"><span data-stu-id="10574-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="10574-108">В их число входят те технологии, которые необходимо знать перед тем, как вы попытаетесь углубиться в.</span><span class="sxs-lookup"><span data-stu-id="10574-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="10574-109">Что следует учитывать при разработке игры Windows с помощью DirectX?</span><span class="sxs-lookup"><span data-stu-id="10574-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="10574-110">Перед началом разработки приложения для Магазина Windows с помощью DirectX необходимо знать, как программировать в Windows с использованием C++.</span><span class="sxs-lookup"><span data-stu-id="10574-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="10574-111">Приложения Windows, использующие DirectX, разрабатываются на низком уровне программирования. Это означает, что вы будете предоставлять множество функций операционной системы.</span><span class="sxs-lookup"><span data-stu-id="10574-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="10574-112">К ним относятся управление памятью и ресурсами, а также интерфейс для самого графического устройства.</span><span class="sxs-lookup"><span data-stu-id="10574-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="10574-113">Если вы не знакомы с разработкой игр или графических приложений, это может оказаться непростой задачей.</span><span class="sxs-lookup"><span data-stu-id="10574-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="10574-114">Но вы также получите награду, так как разработка игр на этом уровне создает гораздо больше возможностей для разработки и разработки игр и графических приложений.</span><span class="sxs-lookup"><span data-stu-id="10574-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="10574-115">Вам также потребуется ознакомиться с основами программирования двухмерной и трехмерной графики, так как многие из API-интерфейсов, которые вы будете использовать, были разработаны с учетом этих принципов.</span><span class="sxs-lookup"><span data-stu-id="10574-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="10574-116">Вам будет удобнее понимать свои параметры и результаты, если вы знакомы с операциями, выполняемыми за ними.</span><span class="sxs-lookup"><span data-stu-id="10574-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="10574-117">Как минимум, необходимо иметь в наличии следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="10574-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="10574-118">Программирование в Windows C/C++.</span><span class="sxs-lookup"><span data-stu-id="10574-118">Windows C/C++ programming.</span></span> <span data-ttu-id="10574-119">Это означает, что вы понимаете указатели и ссылки, события и обратные вызовы и, возможно, некоторые из распространенных библиотек, таких как ATL.</span><span class="sxs-lookup"><span data-stu-id="10574-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="10574-120">Программирование Win32.</span><span class="sxs-lookup"><span data-stu-id="10574-120">Win32 programming.</span></span> <span data-ttu-id="10574-121">Вы понимаете, как создаются окна и как обрабатываются события пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="10574-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="10574-122">Кроме того, вы можете немного разобраться с COM и важными API-интерфейсами Win32.</span><span class="sxs-lookup"><span data-stu-id="10574-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="10574-123">Линейная перерезка и тригонометрические функции.</span><span class="sxs-lookup"><span data-stu-id="10574-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="10574-124">Хотя это и не является обязательным, у вас уже есть опыт работы с концепциями из этих двух математических дисциплин, поскольку они являются основой большей части программирования трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="10574-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="10574-125">Базовая терминология и основные понятия графики, такие как точечные рисунки, текстуры, вершины, сетки и окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="10574-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="10574-126">Что предоставляет DirectX?</span><span class="sxs-lookup"><span data-stu-id="10574-126">What does DirectX provide me?</span></span>

<span data-ttu-id="10574-127">DirectX — это основной набор API графических интерфейсов, который будет использоваться для разработки игр Windows.</span><span class="sxs-lookup"><span data-stu-id="10574-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="10574-128">Ниже приведены категории функций, с которыми необходимо ознакомиться при принятии решения о разработке игры.</span><span class="sxs-lookup"><span data-stu-id="10574-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="10574-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="10574-129">Library</span></span>     | <span data-ttu-id="10574-130">Описание</span><span class="sxs-lookup"><span data-stu-id="10574-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10574-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="10574-131">Direct3D</span></span>    | <span data-ttu-id="10574-132">Мощный, ориентированный на производительность набор библиотек с аппаратным ускорением для отрисовки трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="10574-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="10574-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="10574-133">Direct2D</span></span>    | <span data-ttu-id="10574-134">Набор библиотек 2D-графики для точечного рисунка с аппаратным ускорением и векторной двухмерной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="10574-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="10574-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="10574-135">DirectXMath</span></span> | <span data-ttu-id="10574-136">Библиотека распространенных, оптимизированных математических операций, используемых в двухмерной и трехмерной графике, например векторные и матричные операции.</span><span class="sxs-lookup"><span data-stu-id="10574-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="10574-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="10574-137">DirectWrite</span></span> | <span data-ttu-id="10574-138">Библиотека API отрисовки и макета 2D-текста.</span><span class="sxs-lookup"><span data-stu-id="10574-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="10574-139">Он поддерживает аппаратное ускорение и растрирование программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="10574-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="10574-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="10574-140">XAudio2</span></span>     | <span data-ttu-id="10574-141">Многоплатформенный аудио API для Microsoft Windows, обеспечивающий обработку сигнала и микширование звука для разработки игр.</span><span class="sxs-lookup"><span data-stu-id="10574-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="10574-142">XInput</span><span class="sxs-lookup"><span data-stu-id="10574-142">XInput</span></span>      | <span data-ttu-id="10574-143">Библиотека, которая поддерживает различные традиционные игровые элементы управления, с акцентом на модели контроллера Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="10574-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="10574-144">Какие средства мне нужны для разработки игр Windows с помощью DirectX?</span><span class="sxs-lookup"><span data-stu-id="10574-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="10574-145">Чтобы приступить к работе с этим руководством, вам потребуется:</span><span class="sxs-lookup"><span data-stu-id="10574-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="10574-146">Windows 8.1 или выше</span><span class="sxs-lookup"><span data-stu-id="10574-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="10574-147">Microsoft Visual Studio 2013 или выше</span><span class="sxs-lookup"><span data-stu-id="10574-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




