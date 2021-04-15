---
description: Режимы VMR в операции
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Режимы VMR в операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662676"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="82bee-103">Режимы VMR в операции</span><span class="sxs-lookup"><span data-stu-id="82bee-103">VMR Modes of Operation</span></span>

<span data-ttu-id="82bee-104">Архитектура компонента VMR позволяет приложениям настраивать их различными способами в зависимости от того, как выполняется отрисовка.</span><span class="sxs-lookup"><span data-stu-id="82bee-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="82bee-105">В следующей таблице показаны три режима представления и два режима смешивания, а также компоненты, которые существуют для каждой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="82bee-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="82bee-106">Режим</span><span class="sxs-lookup"><span data-stu-id="82bee-106">Mode</span></span>       | <span data-ttu-id="82bee-107">Один поток</span><span class="sxs-lookup"><span data-stu-id="82bee-107">Single Stream</span></span>                                                                     | <span data-ttu-id="82bee-108">Несколько потоков (режим смешения)</span><span class="sxs-lookup"><span data-stu-id="82bee-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82bee-109">Оконные</span><span class="sxs-lookup"><span data-stu-id="82bee-109">Windowed</span></span>   | <span data-ttu-id="82bee-110">Распределитель — единица синхронизации Пресентеркоре</span><span class="sxs-lookup"><span data-stu-id="82bee-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="82bee-111">Диспетчер окон</span><span class="sxs-lookup"><span data-stu-id="82bee-111">Window Manager</span></span><br/> | <span data-ttu-id="82bee-112">миксеркомпоситор\*</span><span class="sxs-lookup"><span data-stu-id="82bee-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="82bee-113">Распределитель-выступающий</span><span class="sxs-lookup"><span data-stu-id="82bee-113">Allocator-presenter</span></span><br/> <span data-ttu-id="82bee-114">Базовая единица синхронизации</span><span class="sxs-lookup"><span data-stu-id="82bee-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="82bee-115">Диспетчер окон</span><span class="sxs-lookup"><span data-stu-id="82bee-115">Window Manager</span></span><br/> |
| <span data-ttu-id="82bee-116">Без окон</span><span class="sxs-lookup"><span data-stu-id="82bee-116">Windowless</span></span> | <span data-ttu-id="82bee-117">Распределитель — единица синхронизации Пресентеркоре</span><span class="sxs-lookup"><span data-stu-id="82bee-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="82bee-118">миксеркомпоситор\*</span><span class="sxs-lookup"><span data-stu-id="82bee-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="82bee-119">Распределитель-выступающий</span><span class="sxs-lookup"><span data-stu-id="82bee-119">Allocator-presenter</span></span><br/> <span data-ttu-id="82bee-120">Базовая единица синхронизации</span><span class="sxs-lookup"><span data-stu-id="82bee-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="82bee-121">Безмодульная обработка</span><span class="sxs-lookup"><span data-stu-id="82bee-121">Renderless</span></span> | <span data-ttu-id="82bee-122">Распределитель — выступающий (предоставляется приложением) основная единица синхронизации</span><span class="sxs-lookup"><span data-stu-id="82bee-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="82bee-123">миксеркомпоситор\*</span><span class="sxs-lookup"><span data-stu-id="82bee-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="82bee-124">Распределитель-выступающий (предоставляется приложением)</span><span class="sxs-lookup"><span data-stu-id="82bee-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="82bee-125">Базовая единица синхронизации</span><span class="sxs-lookup"><span data-stu-id="82bee-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="82bee-126">\* Указывает, что приложение имеет возможность предоставить пользовательский компонент или использовать компонент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82bee-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="82bee-127">Во всех конфигурациях основным моментом, который следует помнить при создании графов фильтров с помощью фильтра VMR, является то, что необходимо настроить VMR перед подключением.</span><span class="sxs-lookup"><span data-stu-id="82bee-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="82bee-128">Для всех конфигураций ПИН-коды не могут динамически добавляться или удаляться после подключения VMR к вышестоящему фильтру, но они могут быть подключены и отключены.</span><span class="sxs-lookup"><span data-stu-id="82bee-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="82bee-129">Если неизвестно, сколько контактов потребуется, необходимо настроить фильтр VMR для максимального числа, которое может потребоваться.</span><span class="sxs-lookup"><span data-stu-id="82bee-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="82bee-130">Наличие неиспользуемых ПИН-кодов ввода в фильтре не приводит к снижению производительности отрисовки.</span><span class="sxs-lookup"><span data-stu-id="82bee-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="82bee-131">В отличие от старого микшера наложения VMR не имеет выходного ПИН-кода, так как не требует отдельного фильтра для управления окнами.</span><span class="sxs-lookup"><span data-stu-id="82bee-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="82bee-132">В следующих разделах описывается настройка VMR для данного режима.</span><span class="sxs-lookup"><span data-stu-id="82bee-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="82bee-133">Режим с окнами VMR (совместимость)</span><span class="sxs-lookup"><span data-stu-id="82bee-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="82bee-134">Режим без окон VMR</span><span class="sxs-lookup"><span data-stu-id="82bee-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="82bee-135">VMR с несколькими потоками (режим смешения)</span><span class="sxs-lookup"><span data-stu-id="82bee-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="82bee-136">Режим смешения YUV</span><span class="sxs-lookup"><span data-stu-id="82bee-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="82bee-137">Позиционирование и перемещение прямоугольников видео в пространстве композиции</span><span class="sxs-lookup"><span data-stu-id="82bee-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="82bee-138">Режим воспроизведения VMR (пользовательский распределитель — выступающие)</span><span class="sxs-lookup"><span data-stu-id="82bee-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="82bee-139">Монопольный режим DirectDraw</span><span class="sxs-lookup"><span data-stu-id="82bee-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




