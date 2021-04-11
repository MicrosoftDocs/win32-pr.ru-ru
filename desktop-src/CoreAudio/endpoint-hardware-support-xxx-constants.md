---
description: '\_ \_ Константы поддержки конечных точек \_ xxx — это флаги поддержки оборудования для устройства конечной точки аудио.'
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Константы ENDPOINT_HARDWARE_SUPPORT_XXX (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142775"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="f55b3-103">\_ \_ Константы поддержки конечных устройств \_ xxx</span><span class="sxs-lookup"><span data-stu-id="f55b3-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="f55b3-104">\_ \_ Константы поддержки конечных точек \_ xxx — это флаги поддержки оборудования для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="f55b3-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="f55b3-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="f55b3-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="f55b3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f55b3-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="f55b3-107"><dt>**Конечная точка \_ \_ \_ Том аппаратной поддержки**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f55b3-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="f55b3-108">Устройство конечной точки аудио поддерживает аппаратный регулятор громкости.</span><span class="sxs-lookup"><span data-stu-id="f55b3-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="f55b3-109"><dt>**Конечная точка \_ АППАРАТная \_ поддержка не \_ поддерживает**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f55b3-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="f55b3-110">Устройство конечной точки аудио поддерживает аппаратный контроль звука.</span><span class="sxs-lookup"><span data-stu-id="f55b3-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="f55b3-111"><dt>**Конечная точка \_ \_ \_ Счетчик аппаратной поддержки**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="f55b3-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="f55b3-112">Устройство конечной точки аудио поддерживает счетчик пикового использования оборудования.</span><span class="sxs-lookup"><span data-stu-id="f55b3-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="f55b3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f55b3-113">Remarks</span></span>

<span data-ttu-id="f55b3-114">Методы [**иаудиоендпоинтволуме:: куерихардваресуппорт**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) и [**Иаудиометеринформатион:: куерихардваресуппорт**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) используют \_ \_ константы поддержки конечных устройств \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="f55b3-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="f55b3-115">Маска поддержки оборудования указывает, какие функции устройство аудио конечная точка реализует в оборудовании.</span><span class="sxs-lookup"><span data-stu-id="f55b3-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="f55b3-116">Маска может быть либо 0, либо битовой или одной или несколькими \_ \_ константами поддержки конечных точек \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="f55b3-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="f55b3-117">Если в маске задан бит, соответствующий определенной \_ поддержке конечной точки \_ \_ xxx Constant, то это означает, что функция, представленная этой константой, реализована на устройстве оборудованием.</span><span class="sxs-lookup"><span data-stu-id="f55b3-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55b3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f55b3-118">Requirements</span></span>



| <span data-ttu-id="f55b3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f55b3-119">Requirement</span></span> | <span data-ttu-id="f55b3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f55b3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f55b3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f55b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f55b3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f55b3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f55b3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f55b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f55b3-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f55b3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f55b3-125">Header</span><span class="sxs-lookup"><span data-stu-id="f55b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55b3-126"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55b3-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f55b3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f55b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55b3-128">Константы аудиоподсистемы Core</span><span class="sxs-lookup"><span data-stu-id="f55b3-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="f55b3-129">**Иаудиоендпоинтволуме:: Куерихардваресуппорт**</span><span class="sxs-lookup"><span data-stu-id="f55b3-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="f55b3-130">**Иаудиометеринформатион:: Куерихардваресуппорт**</span><span class="sxs-lookup"><span data-stu-id="f55b3-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




