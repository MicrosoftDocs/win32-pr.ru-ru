---
title: Изменение высоты и скорости воспроизведения
description: Изменение высоты и скорости воспроизведения
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- волна аудио, шаг
- волна-звуковой интерфейс, шаг
- звуковая волна, скорость воспроизведения
- волна-звуковой интерфейс, скорость воспроизведения
- волна аудио, изменение высоты
- волна-звуковой интерфейс, изменение высоты
- звуковая волна, изменение скорости воспроизведения
- волна-звуковой интерфейс, изменение скорости воспроизведения
- изменение частоты воспроизведения звука аудио
- изменение аудио-сигнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487724"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="2e01d-113">Изменение высоты и скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="2e01d-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="2e01d-114">Некоторые устройства вывода аудио-аудиосигнала могут изменять тон и скорость воспроизведения данных аудио-файлов.</span><span class="sxs-lookup"><span data-stu-id="2e01d-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="2e01d-115">Не все устройства с аудио-волнами поддерживают изменение скорости и скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2e01d-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="2e01d-116">Сведения о том, как определить, поддерживает ли конкретное устройство волновой волны изменения частоты и скорости воспроизведения, см. в разделе [устройства и типы данных](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="2e01d-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="2e01d-117">Ниже приведены различия между изменением высоты и скоростью воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2e01d-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="2e01d-118">Изменение скорости воспроизведения выполняется драйвером устройства и не требует специального оборудования.</span><span class="sxs-lookup"><span data-stu-id="2e01d-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="2e01d-119">Частота выборки не изменяется, но драйвер выполняет интерполяцию, пропуская или синтезированную выборку.</span><span class="sxs-lookup"><span data-stu-id="2e01d-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="2e01d-120">Например, если частота воспроизведения изменяется с коэффициента 2, драйвер пропускает все остальные примеры.</span><span class="sxs-lookup"><span data-stu-id="2e01d-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="2e01d-121">Для изменения этого шага требуется специализированное оборудование.</span><span class="sxs-lookup"><span data-stu-id="2e01d-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="2e01d-122">Скорость воспроизведения и скорость выборки не изменяются.</span><span class="sxs-lookup"><span data-stu-id="2e01d-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="2e01d-123">Windows предоставляет следующие функции для запроса и настройки частоты аудио и воспроизведения звуковых сигналов.</span><span class="sxs-lookup"><span data-stu-id="2e01d-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="2e01d-124">Функция</span><span class="sxs-lookup"><span data-stu-id="2e01d-124">Function</span></span>                                                 | <span data-ttu-id="2e01d-125">Описание</span><span class="sxs-lookup"><span data-stu-id="2e01d-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="2e01d-126">**вавеаутжетпитч**</span><span class="sxs-lookup"><span data-stu-id="2e01d-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="2e01d-127">Получает шаг для указанного выходного устройства аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="2e01d-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="2e01d-128">**вавеаутжетплайбаккрате**</span><span class="sxs-lookup"><span data-stu-id="2e01d-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="2e01d-129">Возвращает скорость воспроизведения для указанного устройства вывода аудио-файлов.</span><span class="sxs-lookup"><span data-stu-id="2e01d-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="2e01d-130">**вавеаутсетпитч**</span><span class="sxs-lookup"><span data-stu-id="2e01d-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="2e01d-131">Задает шаг для указанного выходного устройства аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="2e01d-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="2e01d-132">**вавеаутсетплайбаккрате**</span><span class="sxs-lookup"><span data-stu-id="2e01d-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="2e01d-133">Задает скорость воспроизведения для указанного выходного устройства аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="2e01d-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="2e01d-134">Частота и скорость воспроизведения изменяются коэффициентом, указанным с числом с фиксированной запятой, упакованным в значение даублеворд.</span><span class="sxs-lookup"><span data-stu-id="2e01d-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="2e01d-135">Старшие 16 битов указывают целую часть числа; младшие 16 битов указывают дробную часть.</span><span class="sxs-lookup"><span data-stu-id="2e01d-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="2e01d-136">Например, значение 1,5 представляется как 0x00018000L.</span><span class="sxs-lookup"><span data-stu-id="2e01d-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="2e01d-137">Значение 0,75 представляется в виде 0x0000C000L.</span><span class="sxs-lookup"><span data-stu-id="2e01d-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="2e01d-138">Значение 1,0 (0x00010000) означает, что высота или скорость воспроизведения не меняются.</span><span class="sxs-lookup"><span data-stu-id="2e01d-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 