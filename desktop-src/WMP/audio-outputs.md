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
ms.openlocfilehash: ffb5ebefb3b2bb72e8314c843ce0fe7632f09652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410807"
---
# <a name="audio-outputs"></a><span data-ttu-id="5796b-118">Звуковые выходные данные</span><span class="sxs-lookup"><span data-stu-id="5796b-118">Audio Outputs</span></span>

<span data-ttu-id="5796b-119">Панель управления в Windows XP позволяет пользователю назначить имя устройства DirectSound по умолчанию конкретному выходному устройству.</span><span class="sxs-lookup"><span data-stu-id="5796b-119">The Control Panel in Windows XP enables the user to assign the name Default DirectSound Device to a particular audio output device.</span></span> <span data-ttu-id="5796b-120">В Windows Vista панель управления позволяет пользователю назначить каждому из трех имен (Еконсоле, Емултимедиа и Екоммуникатионс) на устройство вывода звука.</span><span class="sxs-lookup"><span data-stu-id="5796b-120">In Windows Vista, the Control Panel lets the user assign each of three names (eConsole, eMultimedia, and eCommunications) to an audio output device.</span></span> <span data-ttu-id="5796b-121">Все эти имена могут быть назначены разным устройствам, или одному устройству может быть назначено несколько имен.</span><span class="sxs-lookup"><span data-stu-id="5796b-121">These names can all be assigned to different devices, or multiple names can be assigned to the same device.</span></span> <span data-ttu-id="5796b-122">В следующей таблице показано, как проигрыватель Windows Media и элемент управления ActiveX проигрывателя Windows Media выбирают устройства звукового вывода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5796b-122">The following table shows how Windows Media Player and the Windows Media Player ActiveX control choose default audio output devices.</span></span>



|                                      | <span data-ttu-id="5796b-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5796b-123">Windows XP</span></span>                                                                                                                                                                                | <span data-ttu-id="5796b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5796b-124">Windows Vista</span></span>                                                                                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5796b-125">Проигрыватель Windows Media</span><span class="sxs-lookup"><span data-stu-id="5796b-125">Windows Media Player</span></span>                 | <span data-ttu-id="5796b-126">По умолчанию проигрыватель использует звуковое устройство, назначенное как устройство DirectSound по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5796b-126">By default, the Player uses the audio device designated as Default DirectSound Device.</span></span> <span data-ttu-id="5796b-127">Проигрыватель предоставляет диалоговое окно, позволяющее пользователю переключать проигрыватель на другое звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="5796b-127">The Player provides a dialog box that lets the user switch the Player to a different audio device.</span></span> | <span data-ttu-id="5796b-128">По умолчанию проигрыватель использует звуковое устройство, обозначенное как Емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="5796b-128">By default, the Player uses the audio device designated as eMultimedia.</span></span> <span data-ttu-id="5796b-129">Проигрыватель предоставляет диалоговое окно, позволяющее пользователю переключать проигрыватель на другое звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="5796b-129">The Player provides a dialog box that lets the user switch the Player to a different audio device.</span></span> |
| <span data-ttu-id="5796b-130">Элемент управления ActiveX проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="5796b-130">Windows Media Player ActiveX control</span></span> | <span data-ttu-id="5796b-131">По умолчанию элемент управления "проигрыватель" использует звуковое устройство, назначенное как устройство DirectSound по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5796b-131">By default, the Player control uses the audio device designated as Default DirectSound Device.</span></span> <span data-ttu-id="5796b-132">Устройство вывода звука нельзя изменить программным способом.</span><span class="sxs-lookup"><span data-stu-id="5796b-132">The audio output device cannot be changed programmatically.</span></span>                                | <span data-ttu-id="5796b-133">По умолчанию элемент управления "проигрыватель" использует звуковое устройство, обозначенное как Емултимедиа.</span><span class="sxs-lookup"><span data-stu-id="5796b-133">By default, the Player control uses the audio device designated as eMultimedia.</span></span> <span data-ttu-id="5796b-134">Устройство вывода звука нельзя изменить программным способом.</span><span class="sxs-lookup"><span data-stu-id="5796b-134">The audio output device cannot be changed programmatically.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="5796b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5796b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5796b-136">**Проигрыватель Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5796b-136">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




