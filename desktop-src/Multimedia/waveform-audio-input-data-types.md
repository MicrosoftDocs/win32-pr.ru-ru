---
title: Типы входных данных Waveform-Audio
description: Типы входных данных Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- звуковая волна, типы входных данных
- звуковая волна-интерфейс, типы входных данных
- запись аудио звукового сигнала, типы входных данных
- ХВАВЕИН, обработчик
- Структура ВАВЕФОРМАТЕКС
- Структура ВАВЕХДР
- Структура ВАВЕИНКАПС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069935"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="4cc63-110">Типы входных данных Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="4cc63-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="4cc63-111">Для входных функций аудио-сигнала определены следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="4cc63-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="4cc63-112">Тип</span><span class="sxs-lookup"><span data-stu-id="4cc63-112">Type</span></span>                                 | <span data-ttu-id="4cc63-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4cc63-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc63-114">**хвавеин**</span><span class="sxs-lookup"><span data-stu-id="4cc63-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="4cc63-115">Маркер открытого устройства ввода аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="4cc63-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="4cc63-116">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="4cc63-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="4cc63-117">Структура, указывающая форматы данных, поддерживаемые устройством ввода аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="4cc63-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="4cc63-118">Эта структура также используется для устройств вывода аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="4cc63-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="4cc63-119">**вавехдр**</span><span class="sxs-lookup"><span data-stu-id="4cc63-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="4cc63-120">Структура, используемая в качестве заголовка для блока входных данных аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="4cc63-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="4cc63-121">Эта структура также используется для устройств вывода аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="4cc63-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="4cc63-122">**вавеинкапс**</span><span class="sxs-lookup"><span data-stu-id="4cc63-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="4cc63-123">Структура, используемая для получения сведений о возможностях конкретного входного устройства аудио.</span><span class="sxs-lookup"><span data-stu-id="4cc63-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="4cc63-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4cc63-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc63-125">Запись звука звукозаписи</span><span class="sxs-lookup"><span data-stu-id="4cc63-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 