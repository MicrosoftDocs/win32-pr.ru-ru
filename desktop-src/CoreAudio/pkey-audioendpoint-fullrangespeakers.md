---
description: Свойство PKEY \_ аудиоендпоинт \_ фуллранжеспеакерс указывает маску конфигурации канала для всех динамиков с полным диапазоном, подключенных к устройству конечной точки аудио.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142439"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="256ef-103">PKEY \_ аудиоендпоинт \_ фуллранжеспеакерс</span><span class="sxs-lookup"><span data-stu-id="256ef-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="256ef-104">Свойство **PKEY \_ аудиоендпоинт \_ фуллранжеспеакерс** указывает маску конфигурации канала для всех динамиков с полным диапазоном, подключенных к устройству конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="256ef-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="256ef-105">Маска указывает физическую конфигурацию динамиков полного диапазона и задает назначение каналов для этих динамиков.</span><span class="sxs-lookup"><span data-stu-id="256ef-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="256ef-106">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="256ef-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="256ef-107">Элемент **уинтвал** структуры **пропвариант** содержит маску конфигурации канала, которая приведена к типу **uint**.</span><span class="sxs-lookup"><span data-stu-id="256ef-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="256ef-108">Динамики с полным диапазоном позволяют воспроизводить звуки в пределах от басов до высоких частот.</span><span class="sxs-lookup"><span data-stu-id="256ef-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="256ef-109">Обычно крупные динамики имеют полный спектр, но небольшие динамики значительно меньше, чем воспроизведение звуковых сигналов.</span><span class="sxs-lookup"><span data-stu-id="256ef-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="256ef-110">В Windows Vista обработчик звука использует это свойство для управления уровнями басов в потоке вывода звука, который воспроизводится устройством конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="256ef-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="256ef-111">Маска конфигурации канала для этого свойства имеет тот же формат, что и маска настройки канала для свойства [**PKEY \_ аудиоендпоинт \_ фисикалспеакерс**](pkey-audioendpoint-physicalspeakers.md) .</span><span class="sxs-lookup"><span data-stu-id="256ef-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="256ef-112">Дополнительные сведения о масках конфигурации канала см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="256ef-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="256ef-113">Описание \_ \_ Свойства настройки кспроперти Audio Channel \_ в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="256ef-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="256ef-114">Технический документ под названием "Поддержка аудио драйверов для конфигураций динамиков домашнего кинотеатра" на веб-сайте [технологии аудио устройства для Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="256ef-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="256ef-115">Система получает маску конфигурации канала для \_ Свойства PKEY аудиоендпоинт \_ фуллранжеспеакерс от пользователя.</span><span class="sxs-lookup"><span data-stu-id="256ef-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="256ef-116">Пользователь вводит эту информацию с помощью панели управления Windows мультимедиа, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="256ef-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="256ef-117">Дополнительные сведения о Mmsys.cpl см. в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="256ef-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="256ef-118">Маска конфигурации канала для \_ Свойства PKEY аудиоендпоинт \_ фуллранжеспеакерс устройства конечной точки аудио является подмножеством маски настройки канала для \_ Свойства PKEY аудиоендпоинт \_ фисикалспеакерс этого же устройства.</span><span class="sxs-lookup"><span data-stu-id="256ef-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="256ef-119">Например, если устройство конечной точки аудио управляет набором динамиков с объемом звука 5,1, то маска настройки канала для \_ Свойства PKEY аудиоендпоинт \_ ФИСИКАЛСПЕАКЕРС — ксаудио \_ динамика \_ 5POINT1.</span><span class="sxs-lookup"><span data-stu-id="256ef-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="256ef-120">Эта маска указывает на присутствие передних левый, передних правых, передних правых и боковых динамиков, а также сабвуфера.</span><span class="sxs-lookup"><span data-stu-id="256ef-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="256ef-121">Если передний левый и передний правый динамики достаточно велики для воспроизведения звуковых сигналов, но небольшие динамики не отображаются, то для свойства PKEY аудиоендпоинт фуллранжеспеакерс используется маска настройки канала — \_ \_ ксаудио \_ \_ стерео стереосистема, которая указывает только передний левый и передний правый динамики.</span><span class="sxs-lookup"><span data-stu-id="256ef-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="256ef-122">Канал — маски конфигурации КСАУДИО \_ динамика \_ 5POINT1 и ксаудио \_ \_ , которые определяются в файле заголовка ксмедиа. h.</span><span class="sxs-lookup"><span data-stu-id="256ef-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="256ef-123">Требования</span><span class="sxs-lookup"><span data-stu-id="256ef-123">Requirements</span></span>



| <span data-ttu-id="256ef-124">Требование</span><span class="sxs-lookup"><span data-stu-id="256ef-124">Requirement</span></span> | <span data-ttu-id="256ef-125">Значение</span><span class="sxs-lookup"><span data-stu-id="256ef-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="256ef-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="256ef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="256ef-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="256ef-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="256ef-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="256ef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="256ef-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="256ef-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="256ef-130">Header</span><span class="sxs-lookup"><span data-stu-id="256ef-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="256ef-131"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="256ef-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256ef-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="256ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256ef-133">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="256ef-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="256ef-134">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="256ef-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="256ef-135">**\_Свойство PKEY аудиоендпоинт \_ фисикалспеакерс**</span><span class="sxs-lookup"><span data-stu-id="256ef-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




