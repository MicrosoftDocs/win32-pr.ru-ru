---
title: Начало работы с DirectX для Windows
description: Создание игры Microsoft DirectX для Windows — это задача нового разработчика. Здесь мы быстро рассмотрим связанные понятия и действия, которые необходимо предпринять, чтобы начать разработку игры с помощью DirectX и C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700881"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="aef1e-104">Начало работы с DirectX для Windows</span><span class="sxs-lookup"><span data-stu-id="aef1e-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="aef1e-105">Создание игры Microsoft DirectX для Windows — это задача нового разработчика.</span><span class="sxs-lookup"><span data-stu-id="aef1e-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="aef1e-106">Здесь мы быстро рассмотрим связанные понятия и действия, которые необходимо предпринять, чтобы начать разработку игры с помощью DirectX и C++.</span><span class="sxs-lookup"><span data-stu-id="aef1e-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="aef1e-107">Давайте приступим.</span><span class="sxs-lookup"><span data-stu-id="aef1e-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="aef1e-108">Какие навыки вам нужны?</span><span class="sxs-lookup"><span data-stu-id="aef1e-108">What skills do you need?</span></span>

<span data-ttu-id="aef1e-109">Для разработки игр в DirectX для Windows необходимо иметь несколько основных навыков.</span><span class="sxs-lookup"><span data-stu-id="aef1e-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="aef1e-110">В частности, у вас должна быть возможность:</span><span class="sxs-lookup"><span data-stu-id="aef1e-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="aef1e-111">Чтение и запись современного кода C++ (C++ 11 помогает наиболее эффективно) и знакомство с базовыми принципами и шаблонами разработки C++, такими как шаблоны и модель фабрики.</span><span class="sxs-lookup"><span data-stu-id="aef1e-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="aef1e-112">Также необходимо ознакомиться с распространенными библиотеками C++, такими как стандартная библиотека шаблонов, а именно с операторами приведения, типами указателей и структурами данных стандартной библиотеки шаблонов (например, std:: Vector).</span><span class="sxs-lookup"><span data-stu-id="aef1e-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="aef1e-113">Общие сведения об основных геометрических, тригонометрических и линейных.</span><span class="sxs-lookup"><span data-stu-id="aef1e-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="aef1e-114">Большая часть кода, который вы найдете в примерах, предполагает, что вы понимаете эти формы математики и их общие правила.</span><span class="sxs-lookup"><span data-stu-id="aef1e-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="aef1e-115">Знакомство с COM, особенно [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (интеллектуальный указатель).</span><span class="sxs-lookup"><span data-stu-id="aef1e-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="aef1e-116">Ознакомьтесь с основами графики и графических технологий, особенно трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="aef1e-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="aef1e-117">Хотя собственно DirectX имеет собственную терминологию, он по-прежнему строится на основе хорошо установленного понимания общих принципов трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="aef1e-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="aef1e-118">Понимание концепции цикла обработки сообщений, так как вы будете реализовывать цикл, который прослушивает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="aef1e-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="aef1e-119">И мы отключены!</span><span class="sxs-lookup"><span data-stu-id="aef1e-119">And we're off!</span></span>

<span data-ttu-id="aef1e-120">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="aef1e-120">Ready to start?</span></span> <span data-ttu-id="aef1e-121">Давайте посмотрим перед тем, как мы будем зашлем.</span><span class="sxs-lookup"><span data-stu-id="aef1e-121">Let's review before we head on.</span></span> <span data-ttu-id="aef1e-122">Вы выполнили следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="aef1e-122">You have:</span></span>

-   <span data-ttu-id="aef1e-123">Обновленная и Рабочая установка Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="aef1e-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="aef1e-124">Установка [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="aef1e-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="aef1e-125">Встретилсяе и желание узнать больше о разработке игр DirectX!</span><span class="sxs-lookup"><span data-stu-id="aef1e-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="aef1e-126">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="aef1e-126">Next steps</span></span>



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aef1e-127">Работа с ресурсами устройств DirectX</span><span class="sxs-lookup"><span data-stu-id="aef1e-127">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="aef1e-128">Узнайте, как использовать DXGI для создания виртуализированного графического устройства, а затем создать и настроить цепочку буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="aef1e-128">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="aef1e-129">Общие сведения о конвейере визуализации Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="aef1e-129">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="aef1e-130">Узнайте, как присоединиться к классу ресурсов DirectX-устройства и рисовать с помощью графического конвейера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aef1e-130">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="aef1e-131">Работа с шейдерами и ресурсами шейдера</span><span class="sxs-lookup"><span data-stu-id="aef1e-131">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="aef1e-132">Узнайте, как писать программы шейдера HLSL для этапов графического конвейера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aef1e-132">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 