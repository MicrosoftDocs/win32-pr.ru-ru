---
description: Свойство PKEY \_ аудиоендпоинт \_ формфактор указывает конструктивный параметр устройства конечной точки аудио. Форм фактор указывает физические атрибуты устройства аудио конечных точек, которыми управляет пользователь.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496515"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="3e079-104">PKEY \_ аудиоендпоинт \_ формфактор</span><span class="sxs-lookup"><span data-stu-id="3e079-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="3e079-105">Свойство **PKEY \_ аудиоендпоинт \_ формфактор** указывает конструктивный параметр устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="3e079-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="3e079-106">Форм фактор указывает физические атрибуты устройства аудио конечных точек, которыми управляет пользователь.</span><span class="sxs-lookup"><span data-stu-id="3e079-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="3e079-107">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="3e079-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="3e079-108">Элемент **уинтвал** структуры **пропвариант** содержит значение перечисления, приведенное к типу uint.</span><span class="sxs-lookup"><span data-stu-id="3e079-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="3e079-109">Для него задано одно из следующих значений перечисления [**ендпоинтформфактор**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) :</span><span class="sxs-lookup"><span data-stu-id="3e079-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="3e079-110">ремотенетворкдевице</span><span class="sxs-lookup"><span data-stu-id="3e079-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="3e079-111">Speakers</span><span class="sxs-lookup"><span data-stu-id="3e079-111">Speakers</span></span>
-   <span data-ttu-id="3e079-112">линелевел</span><span class="sxs-lookup"><span data-stu-id="3e079-112">LineLevel</span></span>
-   <span data-ttu-id="3e079-113">Наушники</span><span class="sxs-lookup"><span data-stu-id="3e079-113">Headphones</span></span>
-   <span data-ttu-id="3e079-114">Микрофон</span><span class="sxs-lookup"><span data-stu-id="3e079-114">Microphone</span></span>
-   <span data-ttu-id="3e079-115">Headset</span><span class="sxs-lookup"><span data-stu-id="3e079-115">Headset</span></span>
-   <span data-ttu-id="3e079-116">Трубк</span><span class="sxs-lookup"><span data-stu-id="3e079-116">Handset</span></span>
-   <span data-ttu-id="3e079-117">ункновндигиталпасссраугх</span><span class="sxs-lookup"><span data-stu-id="3e079-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="3e079-118">SPDIF</span><span class="sxs-lookup"><span data-stu-id="3e079-118">SPDIF</span></span>
-   <span data-ttu-id="3e079-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="3e079-119">HDMI</span></span>
-   <span data-ttu-id="3e079-120">ункновнформфактор</span><span class="sxs-lookup"><span data-stu-id="3e079-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="3e079-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3e079-121">Requirements</span></span>



| <span data-ttu-id="3e079-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3e079-122">Requirement</span></span> | <span data-ttu-id="3e079-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3e079-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e079-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e079-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3e079-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e079-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e079-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e079-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3e079-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e079-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e079-128">Header</span><span class="sxs-lookup"><span data-stu-id="3e079-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e079-129"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e079-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e079-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e079-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e079-131">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="3e079-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="3e079-132">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="3e079-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




