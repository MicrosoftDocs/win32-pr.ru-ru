---
title: Изменение объема Waveform-Audio воспроизведения
description: Изменение объема Waveform-Audio воспроизведения
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- звуковая волна, изменение громкости воспроизведения
- аудио-интерфейс, изменение громкости воспроизведения
- звуковая волна, громкость воспроизведения
- волна-звуковой интерфейс, громкость воспроизведения
- Изменение звукового тома воспроизведения аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791635"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="554f7-108">Изменение объема Waveform-Audio воспроизведения</span><span class="sxs-lookup"><span data-stu-id="554f7-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="554f7-109">Windows предоставляет следующие функции для запроса и установки уровня громкости выходного устройства аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="554f7-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="554f7-110">Функция</span><span class="sxs-lookup"><span data-stu-id="554f7-110">Function</span></span>                                     | <span data-ttu-id="554f7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="554f7-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="554f7-112">**вавеаутжетволуме**</span><span class="sxs-lookup"><span data-stu-id="554f7-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="554f7-113">Возвращает текущий уровень громкости указанного выходного устройства аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="554f7-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="554f7-114">**вавеаутсетволуме**</span><span class="sxs-lookup"><span data-stu-id="554f7-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="554f7-115">Задает уровень громкости для указанного выходного устройства аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="554f7-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="554f7-116">Не все устройства с аудио-волнами поддерживают изменения томов.</span><span class="sxs-lookup"><span data-stu-id="554f7-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="554f7-117">Некоторые устройства поддерживают отдельный регулятор громкости как по левому, так и по правому каналам.</span><span class="sxs-lookup"><span data-stu-id="554f7-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="554f7-118">Сведения о том, как определить возможности управления томами для устройств аудио-аудиосигнала, см. в разделе [устройства и типы данных](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="554f7-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="554f7-119">Некоторые приложения позволяют пользователю управлять томом для всех звуковых устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="554f7-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="554f7-120">(Многие приложения этого типа используют службы микшера звука; дополнительные сведения см. в статье [Audio миксерс](audio-mixers.md).) Если приложение не поддерживает этот тип главного регулятора, перед изменением тома следует открыть звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="554f7-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="554f7-121">Необходимо также запросить уровень громкости перед его изменением и восстановить предыдущий уровень громкости как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="554f7-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="554f7-122">Том указан в значении даублеворд.</span><span class="sxs-lookup"><span data-stu-id="554f7-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="554f7-123">Если формат звукового сигнала — стерео, верхние 16 бит указывают относительный том правого канала, а младшие 16 бит указывают относительный объем левого канала.</span><span class="sxs-lookup"><span data-stu-id="554f7-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="554f7-124">Для устройств, которые не поддерживают элемент управления громкостью слева и справа, младшие 16 бит указывают уровень громкости, а верхние 16 бит игнорируются.</span><span class="sxs-lookup"><span data-stu-id="554f7-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="554f7-125">Значения уровня громкости находятся в диапазоне от 0x0 (тишина) до 0xFFFF (максимальный том) и интерпретируемы как пропорциональны логарифму.</span><span class="sxs-lookup"><span data-stu-id="554f7-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="554f7-126">Воспринимаемое увеличение громкости при увеличении уровня громкости с 0x5000 до 0x6000 не отличается от 0x4000 до 0x5000.</span><span class="sxs-lookup"><span data-stu-id="554f7-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 