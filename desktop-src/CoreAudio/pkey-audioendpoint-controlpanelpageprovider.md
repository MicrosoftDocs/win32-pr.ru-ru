---
description: Свойство PKEY \_ аудиоендпоинт \_ контролпанелпажепровидер указывает идентификатор CLSID зарегистрированного поставщика расширения свойств устройства для устройства конечной точки аудио.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895921"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="bf197-103">PKEY \_ аудиоендпоинт \_ контролпанелпажепровидер</span><span class="sxs-lookup"><span data-stu-id="bf197-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="bf197-104">Свойство **PKEY \_ аудиоендпоинт \_ контролпанелпажепровидер** указывает идентификатор CLSID зарегистрированного поставщика расширения свойств устройства для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="bf197-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="bf197-105">Расширение предоставляет свойства конечной точки аудио, отображаемые на странице Свойства устройства панели управления Windows мультимедиа, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="bf197-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="bf197-106">Дополнительные сведения о Mmsys.cpl см. в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="bf197-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="bf197-107">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="bf197-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="bf197-108">Элемент **пвсзвал** структуры **пропвариант** указывает на строку расширенных символов, заканчивающуюся НУЛЕМ, которая содержит идентификатор GUID, определяющий поставщик расширения панели управления.</span><span class="sxs-lookup"><span data-stu-id="bf197-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf197-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bf197-109">Requirements</span></span>



| <span data-ttu-id="bf197-110">Требование</span><span class="sxs-lookup"><span data-stu-id="bf197-110">Requirement</span></span> | <span data-ttu-id="bf197-111">Значение</span><span class="sxs-lookup"><span data-stu-id="bf197-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf197-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf197-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bf197-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf197-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf197-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf197-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bf197-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf197-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf197-116">Header</span><span class="sxs-lookup"><span data-stu-id="bf197-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf197-117"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf197-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf197-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf197-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf197-119">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="bf197-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="bf197-120">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="bf197-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




