---
title: Ошибки Waveform-Audio
description: Ошибки Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Возвращаемые значения МЦИЕРР, ошибки аудио-сигнала
- справочные материалы по мультимедиа, ошибки аудио-сигнала
- Справочник по мультимедиа, ошибкам аудио-сигнала
- Интерфейс управления мультимедиа (MCI), ошибки аудио-сигнала
- MCI (интерфейс управления мультимедиа), ошибки аудио-сигнала
- Справочник по MCI, ошибкам аудио-сигнала
- Справочник MCI, ошибки аудио-сигнала
- Интерфейс управления мультимедиа (MCI), ошибки
- MCI (интерфейс управления мультимедийными файлами), ошибки
- Справочник по MCI, ошибкам
- Ссылка MCI, ошибки
- волна-ошибки аудио
- Звуковая волна MCI — ошибки аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067569"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="117b7-116">Ошибки Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="117b7-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="117b7-117">Для устройств MCI аудио-аудио определены следующие дополнительные возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="117b7-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="117b7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="117b7-118">Value</span></span>                             | <span data-ttu-id="117b7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="117b7-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117b7-120">МЦИЕРР \_ волна \_ инпутсинусе</span><span class="sxs-lookup"><span data-stu-id="117b7-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="117b7-121">Все устройства форм, которые могут записывать файлы в текущем формате, используются.</span><span class="sxs-lookup"><span data-stu-id="117b7-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="117b7-122">Подождите, пока одно из этих устройств освободится; затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="117b7-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="117b7-123">МЦИЕРР \_ волна \_ инпутсунсуитабле</span><span class="sxs-lookup"><span data-stu-id="117b7-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="117b7-124">Ни одно из установленных устройств аудио не может записывать файлы в текущем формате.</span><span class="sxs-lookup"><span data-stu-id="117b7-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="117b7-125">Используйте параметр драйверы на панели управления, чтобы установить подходящее устройство записи аудио.</span><span class="sxs-lookup"><span data-stu-id="117b7-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="117b7-126">МЦИЕРР \_ волна \_ инпутунспеЦифиед</span><span class="sxs-lookup"><span data-stu-id="117b7-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="117b7-127">Можно указать любое совместимое устройство записи аудио.</span><span class="sxs-lookup"><span data-stu-id="117b7-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="117b7-128">МЦИЕРР \_ волна \_ аутпутсинусе</span><span class="sxs-lookup"><span data-stu-id="117b7-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="117b7-129">Все устройства форм аудио, которые могут воспроизводить файлы в текущем формате, используются.</span><span class="sxs-lookup"><span data-stu-id="117b7-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="117b7-130">Подождите, пока одно из этих устройств освободится; затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="117b7-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="117b7-131">МЦИЕРР \_ волна \_ аутпутсунсуитабле</span><span class="sxs-lookup"><span data-stu-id="117b7-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="117b7-132">Ни одно из установленных устройств аудио не может воспроизводить файлы в текущем формате.</span><span class="sxs-lookup"><span data-stu-id="117b7-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="117b7-133">Используйте параметр драйверы на панели управления, чтобы установить подходящее устройство аудио.</span><span class="sxs-lookup"><span data-stu-id="117b7-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="117b7-134">МЦИЕРР \_ волна \_ аутпутунспеЦифиед</span><span class="sxs-lookup"><span data-stu-id="117b7-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="117b7-135">Можно указать любое совместимое устройство воспроизведения аудио.</span><span class="sxs-lookup"><span data-stu-id="117b7-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="117b7-136">МЦИЕРР \_ волна \_ сетинпутинусе</span><span class="sxs-lookup"><span data-stu-id="117b7-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="117b7-137">Текущее устройство аудио уже используется.</span><span class="sxs-lookup"><span data-stu-id="117b7-137">The current waveform device is in use.</span></span> <span data-ttu-id="117b7-138">Подождите, пока устройство освободится; затем повторите попытку, чтобы настроить устройство для записи.</span><span class="sxs-lookup"><span data-stu-id="117b7-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="117b7-139">МЦИЕРР \_ волна \_ сетинпутунсуитабле</span><span class="sxs-lookup"><span data-stu-id="117b7-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="117b7-140">Устройство, используемое для записи волны, не может распознать формат данных.</span><span class="sxs-lookup"><span data-stu-id="117b7-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="117b7-141">МЦИЕРР \_ волна \_ сетаутпутинусе</span><span class="sxs-lookup"><span data-stu-id="117b7-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="117b7-142">Текущее устройство аудио уже используется.</span><span class="sxs-lookup"><span data-stu-id="117b7-142">The current waveform device is in use.</span></span> <span data-ttu-id="117b7-143">Подождите, пока устройство освободится; затем повторите попытку, чтобы задать устройство для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="117b7-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="117b7-144">МЦИЕРР \_ волна \_ сетаутпутунсуитабле</span><span class="sxs-lookup"><span data-stu-id="117b7-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="117b7-145">Устройство, используемое для воспроизведения звуковой волны, не может распознать формат данных.</span><span class="sxs-lookup"><span data-stu-id="117b7-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 




