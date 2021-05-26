---
title: Звуковые выходные данные
description: Звуковые выходные данные
ms.assetid: 2bedf804-c9fd-4a44-9289-e36a50517b7f
keywords:
- Проигрыватель Windows Media, выходные данные аудио
- Проигрыватель Windows Media, устройство DirectSound по умолчанию
- Проигрыватель Windows Media, Еконсоле
- Проигрыватель Windows Media, Емултимедиа
- Проигрыватель Windows Media, Екоммуникатионс
- звуковые выходные данные
- Устройство DirectSound по умолчанию
- еконсоле
- емултимедиа
- екоммуникатионс
- Элемент управления ActiveX проигрывателя Windows Media, выходные данные аудио
- Элемент управления ActiveX проигрывателя Windows Media, устройство DirectSound по умолчанию
- Элемент управления ActiveX проигрывателя Windows Media, Еконсоле
- Элемент управления ActiveX проигрывателя Windows Media, Емултимедиа
- Элемент управления ActiveX проигрывателя Windows Media, Екоммуникатионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b41e5fc3284a054ba7497889eab80ec240c9801
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423864"
---
# <a name="audio-outputs"></a><span data-ttu-id="8c7fb-118">Звуковые выходные данные</span><span class="sxs-lookup"><span data-stu-id="8c7fb-118">Audio Outputs</span></span>

<span data-ttu-id="8c7fb-119">Панель управления в Windows XP позволяет пользователю назначить имя устройства DirectSound по умолчанию конкретному выходному устройству.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-119">The Control Panel in Windows XP enables the user to assign the name Default DirectSound Device to a particular audio output device.</span></span> <span data-ttu-id="8c7fb-120">В Windows Vista панель управления позволяет пользователю назначить каждому из трех имен (Еконсоле, Емултимедиа и Екоммуникатионс) на устройство вывода звука.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-120">In Windows Vista, the Control Panel lets the user assign each of three names (eConsole, eMultimedia, and eCommunications) to an audio output device.</span></span> <span data-ttu-id="8c7fb-121">Все эти имена могут быть назначены разным устройствам, или одному устройству может быть назначено несколько имен.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-121">These names can all be assigned to different devices, or multiple names can be assigned to the same device.</span></span> <span data-ttu-id="8c7fb-122">В следующей таблице показано, как проигрыватель Windows Media и элемент управления ActiveX проигрывателя Windows Media выбирают устройства звукового вывода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-122">The following table shows how Windows Media Player and the Windows Media Player ActiveX control choose default audio output devices.</span></span>



|       &nbsp;                               | <span data-ttu-id="8c7fb-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c7fb-123">Windows XP</span></span>                                                                                                                                                                                | <span data-ttu-id="8c7fb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c7fb-124">Windows Vista</span></span>                                                                                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7fb-125">Проигрыватель Windows Media</span><span class="sxs-lookup"><span data-stu-id="8c7fb-125">Windows Media Player</span></span>                 | <span data-ttu-id="8c7fb-126">По умолчанию проигрыватель использует звуковое устройство, назначенное как устройство DirectSound по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-126">By default, the Player uses the audio device designated as Default DirectSound Device.</span></span> <span data-ttu-id="8c7fb-127">Проигрыватель предоставляет диалоговое окно, позволяющее пользователю переключать проигрыватель на другое звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-127">The Player provides a dialog box that lets the user switch the Player to a different audio device.</span></span> | <span data-ttu-id="8c7fb-128">По умолчанию проигрыватель использует звуковое устройство, обозначенное как Емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-128">By default, the Player uses the audio device designated as eMultimedia.</span></span> <span data-ttu-id="8c7fb-129">Проигрыватель предоставляет диалоговое окно, позволяющее пользователю переключать проигрыватель на другое звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-129">The Player provides a dialog box that lets the user switch the Player to a different audio device.</span></span> |
| <span data-ttu-id="8c7fb-130">Элемент управления ActiveX проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="8c7fb-130">Windows Media Player ActiveX control</span></span> | <span data-ttu-id="8c7fb-131">По умолчанию элемент управления "проигрыватель" использует звуковое устройство, назначенное как устройство DirectSound по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-131">By default, the Player control uses the audio device designated as Default DirectSound Device.</span></span> <span data-ttu-id="8c7fb-132">Устройство вывода звука нельзя изменить программным способом.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-132">The audio output device cannot be changed programmatically.</span></span>                                | <span data-ttu-id="8c7fb-133">По умолчанию элемент управления "проигрыватель" использует звуковое устройство, обозначенное как Емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-133">By default, the Player control uses the audio device designated as eMultimedia.</span></span> <span data-ttu-id="8c7fb-134">Устройство вывода звука нельзя изменить программным способом.</span><span class="sxs-lookup"><span data-stu-id="8c7fb-134">The audio output device cannot be changed programmatically.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="8c7fb-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8c7fb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c7fb-136">**Проигрыватель Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8c7fb-136">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




