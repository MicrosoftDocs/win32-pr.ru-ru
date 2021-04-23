---
title: коммутаторы;
description: коммутаторы;
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- аудио миксерс, элементы управления
- Audio миксерс, коммутаторы
- миксерс, элементы управления
- миксерс, коммутаторы
- переключить элементы управления
- Структура MIXERCONTROLDETAILS_BOOLEAN
- Логический элемент управления
- элемент управления ''Кнопка''
- элемент управления вкл./выкл.
- элемент управления Mono
- элемент управления громкостью
- Расширенный элемент управления стерео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890521"
---
# <a name="switches"></a><span data-ttu-id="047cd-115">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="047cd-115">Switches</span></span>

<span data-ttu-id="047cd-116">Переключатели являются двумя параметрами состояния.</span><span class="sxs-lookup"><span data-stu-id="047cd-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="047cd-117">Эти элементы управления используют [**\_ логическую структуру миксерконтролдетаилс**](/previous-versions//dd757295(v=vs.85)) для извлечения и установки свойств элементов управления.</span><span class="sxs-lookup"><span data-stu-id="047cd-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="047cd-118">В следующей таблице описаны типы переключателей.</span><span class="sxs-lookup"><span data-stu-id="047cd-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="047cd-119">Control</span><span class="sxs-lookup"><span data-stu-id="047cd-119">Control</span></span>         | <span data-ttu-id="047cd-120">Описание</span><span class="sxs-lookup"><span data-stu-id="047cd-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047cd-121">логический</span><span class="sxs-lookup"><span data-stu-id="047cd-121">Boolean</span></span>         | <span data-ttu-id="047cd-122">Универсальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="047cd-122">The generic switch.</span></span> <span data-ttu-id="047cd-123">Для него можно задать значение **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="047cd-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="047cd-124">Кнопка</span><span class="sxs-lookup"><span data-stu-id="047cd-124">Button</span></span>          | <span data-ttu-id="047cd-125">Задайте значение **true** для всех кнопок, обрабатываемых драйвером, как будто они были нажаты.</span><span class="sxs-lookup"><span data-stu-id="047cd-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="047cd-126">Если значение равно **false**, никакие действия не предпринимаются.</span><span class="sxs-lookup"><span data-stu-id="047cd-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="047cd-127">Вкл./выкл.</span><span class="sxs-lookup"><span data-stu-id="047cd-127">On/Off</span></span>          | <span data-ttu-id="047cd-128">Альтернативный параметр, представленный рисунком, отличным от того, который используется для логического коммутатора.</span><span class="sxs-lookup"><span data-stu-id="047cd-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="047cd-129">Его можно установить в значение ON или OFF.</span><span class="sxs-lookup"><span data-stu-id="047cd-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="047cd-130">Mute</span><span class="sxs-lookup"><span data-stu-id="047cd-130">Mute</span></span>            | <span data-ttu-id="047cd-131">Выключает звуковую строку (подавляет поток данных строки) или позволяет воспроизвести звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="047cd-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="047cd-132">Этот параметр часто используется для управления линиями, подающееся в микшер.</span><span class="sxs-lookup"><span data-stu-id="047cd-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="047cd-133">Mono</span><span class="sxs-lookup"><span data-stu-id="047cd-133">Mono</span></span>            | <span data-ttu-id="047cd-134">Переключение между моно и стерео выходными данными для стерео аудио линии.</span><span class="sxs-lookup"><span data-stu-id="047cd-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="047cd-135">Установите значение OFF для воспроизведения стерео данных в виде отдельных каналов.</span><span class="sxs-lookup"><span data-stu-id="047cd-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="047cd-136">Задайте значение ON, чтобы объединить данные из обоих каналов в аудиоустройство Mono.</span><span class="sxs-lookup"><span data-stu-id="047cd-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="047cd-137">Громкости</span><span class="sxs-lookup"><span data-stu-id="047cd-137">Loudness</span></span>        | <span data-ttu-id="047cd-138">Увеличивает низкие громкости для звуковой линии.</span><span class="sxs-lookup"><span data-stu-id="047cd-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="047cd-139">Значение ON, чтобы повысить низкий уровень басов.</span><span class="sxs-lookup"><span data-stu-id="047cd-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="047cd-140">Установите значение Выкл., чтобы задать нормальные уровни громкости.</span><span class="sxs-lookup"><span data-stu-id="047cd-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="047cd-141">Степень увеличения зависит от оборудования.</span><span class="sxs-lookup"><span data-stu-id="047cd-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="047cd-142">Дополнительные сведения см. в документации по устройству микшера.</span><span class="sxs-lookup"><span data-stu-id="047cd-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="047cd-143">Расширенное стерео</span><span class="sxs-lookup"><span data-stu-id="047cd-143">Stereo Enhanced</span></span> | <span data-ttu-id="047cd-144">Увеличение стерео цветоделения.</span><span class="sxs-lookup"><span data-stu-id="047cd-144">Increases stereo separation.</span></span> <span data-ttu-id="047cd-145">Задайте значение ON, чтобы увеличить расстояние на стерео.</span><span class="sxs-lookup"><span data-stu-id="047cd-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="047cd-146">Установите значение OFF для параметра без расширения.</span><span class="sxs-lookup"><span data-stu-id="047cd-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 