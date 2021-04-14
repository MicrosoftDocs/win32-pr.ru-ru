---
description: 'Дополнительные сведения: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539212"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="ccd69-103">PKEY \_ аудиоендпоинт \_ фисикалспеакерс</span><span class="sxs-lookup"><span data-stu-id="ccd69-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="ccd69-104">Свойство **PKEY \_ аудиоендпоинт \_ фисикалспеакерс** указывает маску конфигурации канала для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="ccd69-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="ccd69-105">Маска указывает физическую конфигурацию набора докладчиков и задает назначение каналов для колонок.</span><span class="sxs-lookup"><span data-stu-id="ccd69-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="ccd69-106">Дополнительные сведения о масках конфигурации канала см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="ccd69-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="ccd69-107">Описание \_ \_ Свойства настройки кспроперти Audio Channel \_ в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="ccd69-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="ccd69-108">Технический документ под названием "Поддержка аудио драйверов для конфигураций динамиков домашнего кинотеатра" на веб-сайте [технологии аудио устройства для Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="ccd69-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="ccd69-109">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="ccd69-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="ccd69-110">Элемент **уинтвал** структуры **пропвариант** содержит маску конфигурации канала, которая приведена к типу **uint**.</span><span class="sxs-lookup"><span data-stu-id="ccd69-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd69-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ccd69-111">Requirements</span></span>



| <span data-ttu-id="ccd69-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ccd69-112">Requirement</span></span> | <span data-ttu-id="ccd69-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ccd69-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd69-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccd69-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd69-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccd69-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ccd69-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccd69-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd69-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccd69-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ccd69-118">Header</span><span class="sxs-lookup"><span data-stu-id="ccd69-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd69-119"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd69-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd69-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccd69-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd69-121">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="ccd69-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="ccd69-122">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="ccd69-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




