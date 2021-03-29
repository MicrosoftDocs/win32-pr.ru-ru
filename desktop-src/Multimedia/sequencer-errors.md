---
title: Ошибки Sequencer
description: Ошибки Sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- МЦИЕРР возвращаемые значения, ошибки Sequencer
- мультимедийные ссылки, ошибки Sequencer
- Справочник по мультимедиа, ошибкам Sequencer
- Интерфейс управления мультимедиа (MCI), ошибки Sequencer
- MCI (интерфейс управления мультимедиа), ошибки Sequencer
- Справочник по MCI, ошибкам Sequencer
- Справочник MCI, ошибки Sequencer
- Интерфейс управления мультимедиа (MCI), ошибки
- MCI (интерфейс управления мультимедийными файлами), ошибки
- Справочник по MCI, ошибкам
- Ссылка MCI, ошибки
- ошибки Sequencer
- Ошибки секвенсора MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775977"
---
# <a name="sequencer-errors"></a><span data-ttu-id="f6f39-116">Ошибки Sequencer</span><span class="sxs-lookup"><span data-stu-id="f6f39-116">Sequencer Errors</span></span>

<span data-ttu-id="f6f39-117">Для последовательностей MCI определены следующие дополнительные возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="f6f39-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="f6f39-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f6f39-118">Value</span></span>                          | <span data-ttu-id="f6f39-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f6f39-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f39-120">МЦИЕРР \_ Seq \_ div \_ несовместимо</span><span class="sxs-lookup"><span data-stu-id="f6f39-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="f6f39-121">Форматы времени "указатель песни" и SMPTE являются единственными.</span><span class="sxs-lookup"><span data-stu-id="f6f39-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="f6f39-122">Их нельзя использовать вместе.</span><span class="sxs-lookup"><span data-stu-id="f6f39-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="f6f39-123">МЦИЕРР \_ Seq \_ номидипресент</span><span class="sxs-lookup"><span data-stu-id="f6f39-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="f6f39-124">В этой системе нет установленных устройств MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f39-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="f6f39-125">Используйте параметр драйверы на панели управления для установки драйвера MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f39-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="f6f39-126">\_порт мЦиерр \_ Seq \_</span><span class="sxs-lookup"><span data-stu-id="f6f39-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="f6f39-127">Указанный порт MIDI уже используется.</span><span class="sxs-lookup"><span data-stu-id="f6f39-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="f6f39-128">Подождите, пока он освободится; затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="f6f39-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="f6f39-129">МЦИЕРР \_ Seq \_ порт \_ мапнодевице</span><span class="sxs-lookup"><span data-stu-id="f6f39-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="f6f39-130">Текущая программа установки сопоставителя MIDI ссылается на устройство MIDI, которое не установлено в системе.</span><span class="sxs-lookup"><span data-stu-id="f6f39-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="f6f39-131">Используйте средство сопоставления MIDI на панели управления, чтобы изменить настройки.</span><span class="sxs-lookup"><span data-stu-id="f6f39-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="f6f39-132">МЦИЕРР \_ Seq \_ порт \_ мисцеррор</span><span class="sxs-lookup"><span data-stu-id="f6f39-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="f6f39-133">Произошла ошибка с указанным портом.</span><span class="sxs-lookup"><span data-stu-id="f6f39-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="f6f39-134">\_несуществующий \_ порт мЦиерр Seq \_</span><span class="sxs-lookup"><span data-stu-id="f6f39-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="f6f39-135">Указанное устройство MIDI не установлено в системе.</span><span class="sxs-lookup"><span data-stu-id="f6f39-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="f6f39-136">Используйте параметр драйверы на панели управления для установки устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f39-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="f6f39-137">МЦИЕРР \_ Seq \_ портунспеЦифиед</span><span class="sxs-lookup"><span data-stu-id="f6f39-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="f6f39-138">В системе не указан текущий порт MIDI.</span><span class="sxs-lookup"><span data-stu-id="f6f39-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="f6f39-139">\_таймер мЦиерр Seq \_</span><span class="sxs-lookup"><span data-stu-id="f6f39-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="f6f39-140">Все таймеры мультимедиа используются другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="f6f39-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="f6f39-141">Закройте одно из этих приложений. затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="f6f39-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 




