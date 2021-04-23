---
title: Audio Миксерс в Windows Vista
description: Audio Миксерс в Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- мультимедиа аудио, Windows Vista Audio миксерс
- аудио, Windows Vista Audio миксерс
- Audio миксерс, Windows Vista
- миксерс, Windows Vista
- Windows Vista Audio миксерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561614"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="09020-108">Audio Миксерс в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09020-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="09020-109">Начиная с Windows Vista, некоторые элементы управления микшера реализуются в программном обеспечении, а не на оборудовании.</span><span class="sxs-lookup"><span data-stu-id="09020-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="09020-110">Например, элементы управления "Громкость" реализуются с помощью API Windows Audio Session (ВАСАПИ).</span><span class="sxs-lookup"><span data-stu-id="09020-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="09020-111">Эти элементы управления непосредственно не влияют на параметры оборудования.</span><span class="sxs-lookup"><span data-stu-id="09020-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="09020-112">Кроме того, они связаны с звуковым сеансом конкретного процесса, поэтому изменения затрагивают вызывающее приложение, но не влияют на другие приложения.</span><span class="sxs-lookup"><span data-stu-id="09020-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="09020-113">Каждое устройство конечной точки имеет стандартный макет микшера, реализованный в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="09020-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="09020-114">Каждая конечная точка отрисовки аудио содержит одну строку назначения, которая содержит следующее:</span><span class="sxs-lookup"><span data-stu-id="09020-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="09020-115">Элемент управления громкостью</span><span class="sxs-lookup"><span data-stu-id="09020-115">Volume control</span></span>
    -   <span data-ttu-id="09020-116">Отключить контроль</span><span class="sxs-lookup"><span data-stu-id="09020-116">Mute control</span></span>
    -   <span data-ttu-id="09020-117">Исходная строка: звуковые файлы аудио.</span><span class="sxs-lookup"><span data-stu-id="09020-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="09020-118">Исходная строка: аудио компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="09020-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="09020-119">Каждая конечная точка записи звука содержит одну строку назначения, которая содержит следующее:</span><span class="sxs-lookup"><span data-stu-id="09020-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="09020-120">Элемент управления громкостью</span><span class="sxs-lookup"><span data-stu-id="09020-120">Volume control</span></span>
    -   <span data-ttu-id="09020-121">Отключить контроль</span><span class="sxs-lookup"><span data-stu-id="09020-121">Mute control</span></span>
    -   <span data-ttu-id="09020-122">Исходная строка: волна — звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="09020-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="09020-123">Тип компонента зависит от устройства ввода, например микрофона.</span><span class="sxs-lookup"><span data-stu-id="09020-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="09020-124">Каждая строка исходного кода содержит элемент управления "том" и "отключить".</span><span class="sxs-lookup"><span data-stu-id="09020-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="09020-125">На следующей диаграмме показаны компоненты отрисовки конечных точек и конечных точек записи.</span><span class="sxs-lookup"><span data-stu-id="09020-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![макеты микшера по умолчанию](images/mixer1.gif)

<span data-ttu-id="09020-127">Все элементы управления для конечной точки управляют одним и тем же базовым элементом управления программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="09020-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="09020-128">Поэтому при изменении параметров одного элемента управления вы получите уведомление об изменении элемента управления для других элементов управления.</span><span class="sxs-lookup"><span data-stu-id="09020-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="09020-129">(См. раздел [**mm \_ миксм \_ Control \_ Change**](mm-mixm-control-change.md).)</span><span class="sxs-lookup"><span data-stu-id="09020-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="09020-130">Этот стандартный макет предназначен для совместимости с существующими приложениями, которые используют функции микшера звука.</span><span class="sxs-lookup"><span data-stu-id="09020-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="09020-131">Новые приложения должны избегать использования этих функций.</span><span class="sxs-lookup"><span data-stu-id="09020-131">New applications should avoid using these functions.</span></span>

 

 




