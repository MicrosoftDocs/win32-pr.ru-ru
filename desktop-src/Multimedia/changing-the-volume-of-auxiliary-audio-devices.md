---
title: Изменение объема дополнительного Audio-Devices
description: Изменение объема дополнительного Audio-Devices
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- Звукозапись, изменение дополнительного тома звукового устройства
- изменение дополнительного тома звукового устройства
- вспомогательный звук, изменение громкости устройства
- вспомогательный звуковой интерфейс
- вспомогательные аудиоустройства, изменение тома
- Вспомогательное аудио, интерфейс
- Вспомогательные аудио, устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791640"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="b8b7f-110">Изменение объема дополнительного Audio-Devices</span><span class="sxs-lookup"><span data-stu-id="b8b7f-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="b8b7f-111">Windows предоставляет следующие функции для запроса и настройки тома для вспомогательных звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="b8b7f-112">Функция</span><span class="sxs-lookup"><span data-stu-id="b8b7f-112">Function</span></span>                             | <span data-ttu-id="b8b7f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b8b7f-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b8b7f-114">**ауксжетволуме**</span><span class="sxs-lookup"><span data-stu-id="b8b7f-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="b8b7f-115">Возвращает текущий параметр тома указанного вспомогательного устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="b8b7f-116">**аукссетволуме**</span><span class="sxs-lookup"><span data-stu-id="b8b7f-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="b8b7f-117">Задает объем указанного вспомогательного устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="b8b7f-118">Не все вспомогательные звуковые устройства поддерживают изменения томов.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="b8b7f-119">Некоторые устройства могут поддерживать отдельные изменения томов как в левом, так и в правой канале.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="b8b7f-120">Том указывается в значении даублеворд, как и в случае с функциями управления томами аудио-и MIDI.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="b8b7f-121">Если формат звукового сигнала — стерео, верхние 16 бит указывают относительный том правого канала, а младшие 16 бит указывают относительный объем левого канала.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="b8b7f-122">Для устройств, которые не поддерживают элемент управления громкостью слева и справа, младшие 16 бит указывают уровень громкости, а верхние 16 бит игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="b8b7f-123">Значения уровня громкости находятся в диапазоне от 0x0 (тишина) до 0xFFFF (максимальный том) и интерпретируемы как пропорциональны логарифму.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="b8b7f-124">Воспринимаемое увеличение громкости при увеличении уровня громкости с 0x5000 до 0x6000 не отличается от 0x4000 до 0x5000.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 